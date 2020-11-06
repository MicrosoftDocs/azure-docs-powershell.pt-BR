---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 7fb55457f62ceb03cc33b70fa6a8699abe0f6f04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431922"
---
# <span data-ttu-id="94dfc-101">Get-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="94dfc-101">Get-AzureRmRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="94dfc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="94dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="94dfc-103">Obtém as configurações de notificação do Azure site Recovery configuradas para o cofre.</span><span class="sxs-lookup"><span data-stu-id="94dfc-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94dfc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94dfc-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94dfc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="94dfc-105">DESCRIPTION</span></span>
<span data-ttu-id="94dfc-106">O cmdlet **Get-AzureRmRecoveryServicesAsrAlertSetting** Obtém as configurações de notificação do Azure site Recovery configuradas para o cofre.</span><span class="sxs-lookup"><span data-stu-id="94dfc-106">The **Get-AzureRmRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="94dfc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="94dfc-107">EXAMPLES</span></span>

### <span data-ttu-id="94dfc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="94dfc-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="94dfc-109">Configuração de obter alerta/notificação para a recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="94dfc-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="94dfc-110">OS</span><span class="sxs-lookup"><span data-stu-id="94dfc-110">PARAMETERS</span></span>

### <span data-ttu-id="94dfc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94dfc-111">-DefaultProfile</span></span>
<span data-ttu-id="94dfc-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="94dfc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94dfc-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94dfc-113">CommonParameters</span></span>
<span data-ttu-id="94dfc-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94dfc-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94dfc-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94dfc-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94dfc-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="94dfc-116">INPUTS</span></span>

### <span data-ttu-id="94dfc-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="94dfc-117">None</span></span>

## <span data-ttu-id="94dfc-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="94dfc-118">OUTPUTS</span></span>

### <span data-ttu-id="94dfc-119">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRAlertSetting, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="94dfc-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="94dfc-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="94dfc-120">NOTES</span></span>

## <span data-ttu-id="94dfc-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94dfc-121">RELATED LINKS</span></span>
