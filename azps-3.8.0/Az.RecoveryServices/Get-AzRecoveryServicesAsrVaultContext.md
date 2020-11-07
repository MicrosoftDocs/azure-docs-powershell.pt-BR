---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: cc8f5028a5b2d4917e94ebc666c478ee8d04efa7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940899"
---
# <span data-ttu-id="60a0d-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="60a0d-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="60a0d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60a0d-102">SYNOPSIS</span></span>
<span data-ttu-id="60a0d-103">Obtém as informações de configurações do cofre ASR para o cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="60a0d-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="60a0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60a0d-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60a0d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="60a0d-105">DESCRIPTION</span></span>
<span data-ttu-id="60a0d-106">O cmdlet **Get-AzRecoveryServicesAsrVaultContext** Obtém as informações de configurações do cofre ASR relacionadas ao cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="60a0d-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="60a0d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60a0d-107">EXAMPLES</span></span>

### <span data-ttu-id="60a0d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="60a0d-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="60a0d-109">Obtém as configurações do cofre ASR para o cofre de serviços de recuperação (sessão do PowerShell) ativo no momento.</span><span class="sxs-lookup"><span data-stu-id="60a0d-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="60a0d-110">OS</span><span class="sxs-lookup"><span data-stu-id="60a0d-110">PARAMETERS</span></span>

### <span data-ttu-id="60a0d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a0d-111">-DefaultProfile</span></span>
<span data-ttu-id="60a0d-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="60a0d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60a0d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a0d-113">CommonParameters</span></span>
<span data-ttu-id="60a0d-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60a0d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a0d-115">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60a0d-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a0d-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="60a0d-116">INPUTS</span></span>

### <span data-ttu-id="60a0d-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="60a0d-117">None</span></span>

## <span data-ttu-id="60a0d-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="60a0d-118">OUTPUTS</span></span>

### <span data-ttu-id="60a0d-119">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="60a0d-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="60a0d-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="60a0d-120">NOTES</span></span>

## <span data-ttu-id="60a0d-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60a0d-121">RELATED LINKS</span></span>
