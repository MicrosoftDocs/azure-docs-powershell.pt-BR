---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: cc8f5028a5b2d4917e94ebc666c478ee8d04efa7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117224"
---
# <span data-ttu-id="1fe49-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="1fe49-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="1fe49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1fe49-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe49-103">Obtém informações de configurações do cofre ASR para o cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="1fe49-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="1fe49-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1fe49-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fe49-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1fe49-105">DESCRIPTION</span></span>
<span data-ttu-id="1fe49-106">O cmdlet **Get-AzRecoveryServicesAsrVaultContext** obtém informações de configurações de cofre ASR relacionadas ao cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="1fe49-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="1fe49-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1fe49-107">EXAMPLES</span></span>

### <span data-ttu-id="1fe49-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1fe49-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="1fe49-109">Obtém as configurações do cofre ASR para o cofre dos Serviços de Recuperação atualmente ativos (na sessão do PowerShell).</span><span class="sxs-lookup"><span data-stu-id="1fe49-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="1fe49-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1fe49-110">PARAMETERS</span></span>

### <span data-ttu-id="1fe49-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fe49-111">-DefaultProfile</span></span>
<span data-ttu-id="1fe49-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1fe49-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fe49-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fe49-113">CommonParameters</span></span>
<span data-ttu-id="1fe49-114">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fe49-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fe49-115">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1fe49-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fe49-116">Entradas</span><span class="sxs-lookup"><span data-stu-id="1fe49-116">INPUTS</span></span>

### <span data-ttu-id="1fe49-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1fe49-117">None</span></span>

## <span data-ttu-id="1fe49-118">Saídas</span><span class="sxs-lookup"><span data-stu-id="1fe49-118">OUTPUTS</span></span>

### <span data-ttu-id="1fe49-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="1fe49-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="1fe49-120">Notas</span><span class="sxs-lookup"><span data-stu-id="1fe49-120">NOTES</span></span>

## <span data-ttu-id="1fe49-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1fe49-121">RELATED LINKS</span></span>
