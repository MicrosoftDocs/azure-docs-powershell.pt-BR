---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceVaultSecretGroupObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
ms.openlocfilehash: f4d45cddd893ece419fab38759425bb104b64522
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890878"
---
# <span data-ttu-id="d449d-101">New-AzCloudServiceVaultSecretGroupObject</span><span class="sxs-lookup"><span data-stu-id="d449d-101">New-AzCloudServiceVaultSecretGroupObject</span></span>

## <span data-ttu-id="d449d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d449d-102">SYNOPSIS</span></span>
<span data-ttu-id="d449d-103">Criar um objeto na memória para o Grupo Secreto do Vault</span><span class="sxs-lookup"><span data-stu-id="d449d-103">Create a in-memory object for Vault Secret Group</span></span>

## <span data-ttu-id="d449d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d449d-104">SYNTAX</span></span>

```
New-AzCloudServiceVaultSecretGroupObject [-CertificateUrl <String[]>] [-Id <String>] [<CommonParameters>]
```

## <span data-ttu-id="d449d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d449d-105">DESCRIPTION</span></span>
<span data-ttu-id="d449d-106">Criar um objeto na memória para o Grupo Secreto</span><span class="sxs-lookup"><span data-stu-id="d449d-106">Create a in-memory object for Secret Group</span></span>

## <span data-ttu-id="d449d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d449d-107">EXAMPLES</span></span>

### <span data-ttu-id="d449d-108">Exemplo 1: Criar objeto de grupo secreto do cofre</span><span class="sxs-lookup"><span data-stu-id="d449d-108">Example 1: Create vault secret group object</span></span>
```powershell
$keyVault = Get-AzKeyVault -VaultName 'ContosoKeyVault'
$certificate = Get-AzKeyVaultCertificate -VaultName 'ContosoKeyVault' -Name 'ContosoCert'
$secretGroup = New-AzCloudServiceVaultSecretGroupObject -Id $keyVault.ResourceId -CertificateUrl $certificate.SecretId
```

<span data-ttu-id="d449d-109">Este comando cria um objeto de grupo secreto do cofre que é usado para criar ou atualizar um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="d449d-109">This command creates vault secret group object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="d449d-110">Para obter mais detalhes, consulte New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="d449d-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="d449d-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d449d-111">PARAMETERS</span></span>

### <span data-ttu-id="d449d-112">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="d449d-112">-CertificateUrl</span></span>
<span data-ttu-id="d449d-113">Esta é a URL de um certificado que foi carregado no Cofre de Chaves como segredo.</span><span class="sxs-lookup"><span data-stu-id="d449d-113">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d449d-114">-Id</span><span class="sxs-lookup"><span data-stu-id="d449d-114">-Id</span></span>
<span data-ttu-id="d449d-115">ID de Recurso do Cofre de Chaves.</span><span class="sxs-lookup"><span data-stu-id="d449d-115">Key Vault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d449d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d449d-116">CommonParameters</span></span>
<span data-ttu-id="d449d-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d449d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d449d-118">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d449d-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d449d-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d449d-119">INPUTS</span></span>

## <span data-ttu-id="d449d-120">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d449d-120">OUTPUTS</span></span>

### <span data-ttu-id="d449d-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceVaultSecretGroup</span><span class="sxs-lookup"><span data-stu-id="d449d-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceVaultSecretGroup</span></span>

## <span data-ttu-id="d449d-122">NOTES</span><span class="sxs-lookup"><span data-stu-id="d449d-122">NOTES</span></span>

<span data-ttu-id="d449d-123">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d449d-123">ALIASES</span></span>

## <span data-ttu-id="d449d-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d449d-124">RELATED LINKS</span></span>

