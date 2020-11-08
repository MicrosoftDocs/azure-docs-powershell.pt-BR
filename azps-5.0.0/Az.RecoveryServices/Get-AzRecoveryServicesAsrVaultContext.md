---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: cc8f5028a5b2d4917e94ebc666c478ee8d04efa7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118055"
---
# <span data-ttu-id="83d8c-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="83d8c-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="83d8c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="83d8c-102">SYNOPSIS</span></span>
<span data-ttu-id="83d8c-103">Obtém as informações de configurações do cofre ASR para o cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="83d8c-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="83d8c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="83d8c-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83d8c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="83d8c-105">DESCRIPTION</span></span>
<span data-ttu-id="83d8c-106">O cmdlet **Get-AzRecoveryServicesAsrVaultContext** Obtém as informações de configurações do cofre ASR relacionadas ao cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="83d8c-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="83d8c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="83d8c-107">EXAMPLES</span></span>

### <span data-ttu-id="83d8c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="83d8c-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="83d8c-109">Obtém as configurações do cofre ASR para o cofre de serviços de recuperação (sessão do PowerShell) ativo no momento.</span><span class="sxs-lookup"><span data-stu-id="83d8c-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="83d8c-110">OS</span><span class="sxs-lookup"><span data-stu-id="83d8c-110">PARAMETERS</span></span>

### <span data-ttu-id="83d8c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83d8c-111">-DefaultProfile</span></span>
<span data-ttu-id="83d8c-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="83d8c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83d8c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d8c-113">CommonParameters</span></span>
<span data-ttu-id="83d8c-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83d8c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83d8c-115">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83d8c-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d8c-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="83d8c-116">INPUTS</span></span>

### <span data-ttu-id="83d8c-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="83d8c-117">None</span></span>

## <span data-ttu-id="83d8c-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="83d8c-118">OUTPUTS</span></span>

### <span data-ttu-id="83d8c-119">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="83d8c-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="83d8c-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="83d8c-120">NOTES</span></span>

## <span data-ttu-id="83d8c-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="83d8c-121">RELATED LINKS</span></span>
