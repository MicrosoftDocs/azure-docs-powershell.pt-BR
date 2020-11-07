---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 2c1d5254d8705d6511d25038e64107a8199496fb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778212"
---
# <span data-ttu-id="ec8af-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="ec8af-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="ec8af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ec8af-102">SYNOPSIS</span></span>
<span data-ttu-id="ec8af-103">Obtém as configurações de notificação do Azure site Recovery configuradas para o cofre.</span><span class="sxs-lookup"><span data-stu-id="ec8af-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="ec8af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ec8af-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec8af-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ec8af-105">DESCRIPTION</span></span>
<span data-ttu-id="ec8af-106">O cmdlet **Get-AzRecoveryServicesAsrAlertSetting** Obtém as configurações de notificação do Azure site Recovery configuradas para o cofre.</span><span class="sxs-lookup"><span data-stu-id="ec8af-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="ec8af-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ec8af-107">EXAMPLES</span></span>

### <span data-ttu-id="ec8af-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ec8af-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="ec8af-109">Configuração de obter alerta/notificação para a recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="ec8af-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="ec8af-110">OS</span><span class="sxs-lookup"><span data-stu-id="ec8af-110">PARAMETERS</span></span>

### <span data-ttu-id="ec8af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec8af-111">-DefaultProfile</span></span>
<span data-ttu-id="ec8af-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ec8af-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec8af-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec8af-113">CommonParameters</span></span>
<span data-ttu-id="ec8af-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec8af-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec8af-115">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec8af-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec8af-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ec8af-116">INPUTS</span></span>

### <span data-ttu-id="ec8af-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ec8af-117">None</span></span>

## <span data-ttu-id="ec8af-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ec8af-118">OUTPUTS</span></span>

### <span data-ttu-id="ec8af-119">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="ec8af-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="ec8af-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ec8af-120">NOTES</span></span>

## <span data-ttu-id="ec8af-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ec8af-121">RELATED LINKS</span></span>
