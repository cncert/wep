<template>
    
    <div class="column footer-share">
             <p>&copy; 2018 <a href="#"></a></p>
    </div>

</template>

<script>
export default {
    name: 'nav-footer'
}
</script>


<style>
    
    
    .footer-logo {
        margin: 0 auto;
        width: 164px;
        height: 64px;
    }
    .footer-copyright, .footer-icon {
        line-height: 64px;
    }
    
    .footer-icon .icon {
        font-size: 20px;
        color: #69707a;
        vertical-align: middle;
    }
    .footer-icon a:not(:last-child) {
        margin-right: 10px;
    }
    @media (max-width: 768px) {
        .footer {
            padding: 30px 10px;
        }
        .footer .column {
            padding: 0;
        }
        .footer-copyright {
            line-height: 48px;
            font-size: 12px;
            margin-left: 10px;
        }
        .footer-logo {
            width: 48px;
            height: 48px;
        }
        .footer-icon {
            line-height: 48px;
        }
        .footer-icon .icon {
            font-size: 16px;
        }
        .footer-icon a:not(:last-child) {
            margin-right: 0;
        }
    }
</style>
