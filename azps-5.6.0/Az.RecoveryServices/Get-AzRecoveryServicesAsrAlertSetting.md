---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: cadde5ec773452897aa9c6915a5f3e16f00cfef5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892612"
---
# <span data-ttu-id="d1aa3-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="d1aa3-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="d1aa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="d1aa3-103">Obtém as configurações de notificação de Recuperação de Site do Azure para o cofre.</span><span class="sxs-lookup"><span data-stu-id="d1aa3-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="d1aa3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d1aa3-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1aa3-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d1aa3-105">DESCRIPTION</span></span>
<span data-ttu-id="d1aa3-106">O cmdlet **Get-AzRecoveryServicesAsrAlertSetting** obtém as configurações de notificação de Recuperação de Site do Azure para o cofre.</span><span class="sxs-lookup"><span data-stu-id="d1aa3-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="d1aa3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d1aa3-107">EXAMPLES</span></span>

### <span data-ttu-id="d1aa3-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d1aa3-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="d1aa3-109">Obter Configuração de Alerta/Notificação para Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="d1aa3-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="d1aa3-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d1aa3-110">PARAMETERS</span></span>

### <span data-ttu-id="d1aa3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1aa3-111">-DefaultProfile</span></span>
<span data-ttu-id="d1aa3-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d1aa3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1aa3-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1aa3-113">CommonParameters</span></span>
<span data-ttu-id="d1aa3-114">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1aa3-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1aa3-115">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1aa3-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1aa3-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d1aa3-116">INPUTS</span></span>

### <span data-ttu-id="d1aa3-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d1aa3-117">None</span></span>

## <span data-ttu-id="d1aa3-118">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d1aa3-118">OUTPUTS</span></span>

### <span data-ttu-id="d1aa3-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="d1aa3-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="d1aa3-120">NOTES</span><span class="sxs-lookup"><span data-stu-id="d1aa3-120">NOTES</span></span>

## <span data-ttu-id="d1aa3-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1aa3-121">RELATED LINKS</span></span>
