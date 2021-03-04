---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 62f27b43158f8b01abc7be48cab93f4bb957258b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886146"
---
# <span data-ttu-id="54b71-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="54b71-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="54b71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54b71-102">SYNOPSIS</span></span>
<span data-ttu-id="54b71-103">Obtém informações de configurações do cofre ASR para o cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="54b71-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="54b71-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="54b71-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54b71-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="54b71-105">DESCRIPTION</span></span>
<span data-ttu-id="54b71-106">O cmdlet **Get-AzRecoveryServicesAsrVaultContext** obtém informações de configurações de cofre ASR relacionadas ao cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="54b71-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="54b71-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54b71-107">EXAMPLES</span></span>

### <span data-ttu-id="54b71-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="54b71-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="54b71-109">Obtém as configurações do cofre ASR para o cofre dos Serviços de Recuperação atualmente ativos(na sessão do PowerShell).</span><span class="sxs-lookup"><span data-stu-id="54b71-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="54b71-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="54b71-110">PARAMETERS</span></span>

### <span data-ttu-id="54b71-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54b71-111">-DefaultProfile</span></span>
<span data-ttu-id="54b71-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="54b71-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54b71-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54b71-113">CommonParameters</span></span>
<span data-ttu-id="54b71-114">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54b71-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54b71-115">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54b71-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54b71-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54b71-116">INPUTS</span></span>

### <span data-ttu-id="54b71-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="54b71-117">None</span></span>

## <span data-ttu-id="54b71-118">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="54b71-118">OUTPUTS</span></span>

### <span data-ttu-id="54b71-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="54b71-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="54b71-120">NOTES</span><span class="sxs-lookup"><span data-stu-id="54b71-120">NOTES</span></span>

## <span data-ttu-id="54b71-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54b71-121">RELATED LINKS</span></span>
