---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 2be1ca7de1728d1aed7758cd170cb608c7645f18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439835"
---
# <span data-ttu-id="8afe0-101">Get-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="8afe0-101">Get-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="8afe0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8afe0-102">SYNOPSIS</span></span>
<span data-ttu-id="8afe0-103">Obtém as informações de configurações do cofre ASR para o cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8afe0-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8afe0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8afe0-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8afe0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8afe0-105">DESCRIPTION</span></span>
<span data-ttu-id="8afe0-106">O cmdlet **Get-AzureRmRecoveryServicesAsrVaultContext** Obtém as informações de configurações do cofre ASR relacionadas ao cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8afe0-106">The **Get-AzureRmRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="8afe0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8afe0-107">EXAMPLES</span></span>

### <span data-ttu-id="8afe0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8afe0-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzureRmRecoveryServicesAsrVaultContext
```

<span data-ttu-id="8afe0-109">Obtém as configurações do cofre ASR para o cofre de serviços de recuperação (sessão do PowerShell) ativo no momento.</span><span class="sxs-lookup"><span data-stu-id="8afe0-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="8afe0-110">OS</span><span class="sxs-lookup"><span data-stu-id="8afe0-110">PARAMETERS</span></span>

### <span data-ttu-id="8afe0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8afe0-111">-DefaultProfile</span></span>
<span data-ttu-id="8afe0-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8afe0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8afe0-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8afe0-113">CommonParameters</span></span>
<span data-ttu-id="8afe0-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8afe0-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8afe0-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8afe0-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8afe0-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8afe0-116">INPUTS</span></span>

### <span data-ttu-id="8afe0-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8afe0-117">None</span></span>

## <span data-ttu-id="8afe0-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8afe0-118">OUTPUTS</span></span>

### <span data-ttu-id="8afe0-119">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="8afe0-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="8afe0-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8afe0-120">NOTES</span></span>

## <span data-ttu-id="8afe0-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8afe0-121">RELATED LINKS</span></span>
