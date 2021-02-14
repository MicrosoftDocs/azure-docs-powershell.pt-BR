---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 2c1d5254d8705d6511d25038e64107a8199496fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117241"
---
# <span data-ttu-id="06aac-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="06aac-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="06aac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06aac-102">SYNOPSIS</span></span>
<span data-ttu-id="06aac-103">Obtém as configurações de notificação de Recuperação de Site do Azure configuradas para o cofre.</span><span class="sxs-lookup"><span data-stu-id="06aac-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="06aac-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06aac-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06aac-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="06aac-105">DESCRIPTION</span></span>
<span data-ttu-id="06aac-106">O cmdlet **Get-AzRecoveryServicesAsrAlertSetting** obtém as configurações de notificação de Recuperação de Site do Azure configuradas para o cofre.</span><span class="sxs-lookup"><span data-stu-id="06aac-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="06aac-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="06aac-107">EXAMPLES</span></span>

### <span data-ttu-id="06aac-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="06aac-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="06aac-109">Obter Configuração de Alerta/Notificação para Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="06aac-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="06aac-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06aac-110">PARAMETERS</span></span>

### <span data-ttu-id="06aac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06aac-111">-DefaultProfile</span></span>
<span data-ttu-id="06aac-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="06aac-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06aac-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06aac-113">CommonParameters</span></span>
<span data-ttu-id="06aac-114">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06aac-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06aac-115">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06aac-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06aac-116">Entradas</span><span class="sxs-lookup"><span data-stu-id="06aac-116">INPUTS</span></span>

### <span data-ttu-id="06aac-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="06aac-117">None</span></span>

## <span data-ttu-id="06aac-118">Saídas</span><span class="sxs-lookup"><span data-stu-id="06aac-118">OUTPUTS</span></span>

### <span data-ttu-id="06aac-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="06aac-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="06aac-120">Notas</span><span class="sxs-lookup"><span data-stu-id="06aac-120">NOTES</span></span>

## <span data-ttu-id="06aac-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06aac-121">RELATED LINKS</span></span>
