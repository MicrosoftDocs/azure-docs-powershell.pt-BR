---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: e5bb8a19cb616c9696ec224d8f1d9d25678d9e47
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599717"
---
# <span data-ttu-id="bda86-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="bda86-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="bda86-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bda86-102">SYNOPSIS</span></span>
<span data-ttu-id="bda86-103">Obtém as informações de configurações do cofre ASR para o cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="bda86-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="bda86-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bda86-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bda86-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bda86-105">DESCRIPTION</span></span>
<span data-ttu-id="bda86-106">O cmdlet **Get-AzRecoveryServicesAsrVaultContext** Obtém as informações de configurações do cofre ASR relacionadas ao cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="bda86-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="bda86-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bda86-107">EXAMPLES</span></span>

### <span data-ttu-id="bda86-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bda86-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="bda86-109">Obtém as configurações do cofre ASR para o cofre de serviços de recuperação (sessão do PowerShell) ativo no momento.</span><span class="sxs-lookup"><span data-stu-id="bda86-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="bda86-110">OS</span><span class="sxs-lookup"><span data-stu-id="bda86-110">PARAMETERS</span></span>

### <span data-ttu-id="bda86-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bda86-111">-DefaultProfile</span></span>
<span data-ttu-id="bda86-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bda86-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bda86-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bda86-113">CommonParameters</span></span>
<span data-ttu-id="bda86-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bda86-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bda86-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bda86-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bda86-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bda86-116">INPUTS</span></span>

### <span data-ttu-id="bda86-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="bda86-117">None</span></span>

## <span data-ttu-id="bda86-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bda86-118">OUTPUTS</span></span>

### <span data-ttu-id="bda86-119">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="bda86-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="bda86-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bda86-120">NOTES</span></span>

## <span data-ttu-id="bda86-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bda86-121">RELATED LINKS</span></span>
