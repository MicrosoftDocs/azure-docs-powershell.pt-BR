---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 52535af7a2e7e9282a94c07f62154e42fe807a82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440043"
---
# <span data-ttu-id="16a41-101">Get-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="16a41-101">Get-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="16a41-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16a41-102">SYNOPSIS</span></span>
<span data-ttu-id="16a41-103">Obtém as informações de configurações do cofre ASR para o cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="16a41-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16a41-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16a41-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16a41-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="16a41-105">DESCRIPTION</span></span>
<span data-ttu-id="16a41-106">O cmdlet **Get-AzureRmRecoveryServicesAsrVaultContext** Obtém as informações de configurações do cofre ASR relacionadas ao cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="16a41-106">The **Get-AzureRmRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="16a41-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="16a41-107">EXAMPLES</span></span>

### <span data-ttu-id="16a41-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="16a41-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzureRmRecoveryServicesAsrVaultContext
```

<span data-ttu-id="16a41-109">Obtém as configurações do cofre ASR para o cofre de serviços de recuperação (sessão do PowerShell) ativo no momento.</span><span class="sxs-lookup"><span data-stu-id="16a41-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="16a41-110">OS</span><span class="sxs-lookup"><span data-stu-id="16a41-110">PARAMETERS</span></span>

### <span data-ttu-id="16a41-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16a41-111">-DefaultProfile</span></span>
<span data-ttu-id="16a41-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="16a41-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16a41-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16a41-113">CommonParameters</span></span>
<span data-ttu-id="16a41-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16a41-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16a41-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16a41-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16a41-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="16a41-116">INPUTS</span></span>

### <span data-ttu-id="16a41-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="16a41-117">None</span></span>

## <span data-ttu-id="16a41-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="16a41-118">OUTPUTS</span></span>

### <span data-ttu-id="16a41-119">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="16a41-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="16a41-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="16a41-120">NOTES</span></span>

## <span data-ttu-id="16a41-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16a41-121">RELATED LINKS</span></span>
