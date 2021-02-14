---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceVaultSecretGroupObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
ms.openlocfilehash: 925d29e7d567613bbf10e88c65860ebe2ef40c2e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116901"
---
# <span data-ttu-id="680d4-101">New-AzCloudServiceVaultSecretGroupObject</span><span class="sxs-lookup"><span data-stu-id="680d4-101">New-AzCloudServiceVaultSecretGroupObject</span></span>

## <span data-ttu-id="680d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="680d4-102">SYNOPSIS</span></span>
<span data-ttu-id="680d4-103">Criar um objeto na memória para o Grupo Secreto do Cofre</span><span class="sxs-lookup"><span data-stu-id="680d4-103">Create a in-memory object for Vault Secret Group</span></span>

## <span data-ttu-id="680d4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="680d4-104">SYNTAX</span></span>

```
New-AzCloudServiceVaultSecretGroupObject [-CertificateUrl <String[]>] [-Id <String>] [<CommonParameters>]
```

## <span data-ttu-id="680d4-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="680d4-105">DESCRIPTION</span></span>
<span data-ttu-id="680d4-106">Criar um objeto na memória para o Grupo Secreto</span><span class="sxs-lookup"><span data-stu-id="680d4-106">Create a in-memory object for Secret Group</span></span>

## <span data-ttu-id="680d4-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="680d4-107">EXAMPLES</span></span>

### <span data-ttu-id="680d4-108">Exemplo 1: Criar objeto de grupo de cofre secreto</span><span class="sxs-lookup"><span data-stu-id="680d4-108">Example 1: Create vault secret group object</span></span>
```powershell
$keyVault = Get-AzKeyVault -VaultName 'ContosoKeyVault'
$certificate = Get-AzKeyVaultCertificate -VaultName 'ContosoKeyVault' -Name 'ContosoCert'
$secretGroup = New-AzCloudServiceVaultSecretGroupObject -Id $keyVault.ResourceId -CertificateUrl $certificate.SecretId
```

<span data-ttu-id="680d4-109">Esse comando cria um objeto de grupo secreto do cofre que é usado para criar ou atualizar um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="680d4-109">This command creates vault secret group object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="680d4-110">Para obter mais detalhes, consulte New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="680d4-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="680d4-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="680d4-111">PARAMETERS</span></span>

### <span data-ttu-id="680d4-112">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="680d4-112">-CertificateUrl</span></span>
<span data-ttu-id="680d4-113">Esta é a URL de um certificado que foi carregado para o Cofre de Chaves como um segredo.</span><span class="sxs-lookup"><span data-stu-id="680d4-113">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>

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

### <span data-ttu-id="680d4-114">-ID</span><span class="sxs-lookup"><span data-stu-id="680d4-114">-Id</span></span>
<span data-ttu-id="680d4-115">ID do Recurso do Cofre de Chave.</span><span class="sxs-lookup"><span data-stu-id="680d4-115">Key Vault Resource Id.</span></span>

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

### <span data-ttu-id="680d4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="680d4-116">CommonParameters</span></span>
<span data-ttu-id="680d4-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="680d4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="680d4-118">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="680d4-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="680d4-119">Entradas</span><span class="sxs-lookup"><span data-stu-id="680d4-119">INPUTS</span></span>

## <span data-ttu-id="680d4-120">Saídas</span><span class="sxs-lookup"><span data-stu-id="680d4-120">OUTPUTS</span></span>

### <span data-ttu-id="680d4-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceVaultSecgroup</span><span class="sxs-lookup"><span data-stu-id="680d4-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceVaultSecretGroup</span></span>

## <span data-ttu-id="680d4-122">Notas</span><span class="sxs-lookup"><span data-stu-id="680d4-122">NOTES</span></span>

<span data-ttu-id="680d4-123">Aliases</span><span class="sxs-lookup"><span data-stu-id="680d4-123">ALIASES</span></span>

## <span data-ttu-id="680d4-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="680d4-124">RELATED LINKS</span></span>

