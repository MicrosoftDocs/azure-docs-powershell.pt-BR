---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: e7ce712102ffbb74fd8f19eed544642af5a6ebce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773058"
---
# <span data-ttu-id="de229-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="de229-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="de229-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de229-102">SYNOPSIS</span></span>
<span data-ttu-id="de229-103">Obtém as configurações de notificação do Azure site Recovery configuradas para o cofre.</span><span class="sxs-lookup"><span data-stu-id="de229-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="de229-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de229-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de229-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de229-105">DESCRIPTION</span></span>
<span data-ttu-id="de229-106">O cmdlet **Get-AzRecoveryServicesAsrAlertSetting** Obtém as configurações de notificação do Azure site Recovery configuradas para o cofre.</span><span class="sxs-lookup"><span data-stu-id="de229-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="de229-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de229-107">EXAMPLES</span></span>

### <span data-ttu-id="de229-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="de229-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="de229-109">Configuração de obter alerta/notificação para a recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="de229-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="de229-110">OS</span><span class="sxs-lookup"><span data-stu-id="de229-110">PARAMETERS</span></span>

### <span data-ttu-id="de229-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de229-111">-DefaultProfile</span></span>
<span data-ttu-id="de229-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de229-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de229-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de229-113">CommonParameters</span></span>
<span data-ttu-id="de229-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de229-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de229-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de229-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de229-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de229-116">INPUTS</span></span>

### <span data-ttu-id="de229-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="de229-117">None</span></span>

## <span data-ttu-id="de229-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de229-118">OUTPUTS</span></span>

### <span data-ttu-id="de229-119">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="de229-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="de229-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de229-120">NOTES</span></span>

## <span data-ttu-id="de229-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de229-121">RELATED LINKS</span></span>