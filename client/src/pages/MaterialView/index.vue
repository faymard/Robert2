<template>
    <div class="content">
        <div class="content__main-view">
            <div class="MaterialView">
                <Help :message="help" :error="error" :isLoading="isLoading" />
                <tabs
                    v-if="!isLoading"
                    :onSelect="onSelectTab"
                    :defaultIndex="selectedTabIndex"
                    class="MaterialView__body"
                >
                    <template slot="infos">
                        <i class="fas fa-info-circle" /> {{ $t('informations') }}
                    </template>
                    <template slot="documents">
                        <i class="fas fa-file-pdf" /> {{ $t('documents') }}
                    </template>
                    <tab titleSlot="infos">
                        <Infos :material="material" />
                    </tab>
                    <tab titleSlot="documents">
                        <Documents :material="material" />
                    </tab>
                </tabs>
            </div>
        </div>
    </div>
</template>

<script src="./index.js"></script>
