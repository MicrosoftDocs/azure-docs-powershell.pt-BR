---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d9c783d6fe4047aa1d179cd661c88d13e9c716b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601750"
---
# <span data-ttu-id="47f49-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="47f49-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="47f49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47f49-102">SYNOPSIS</span></span>
<span data-ttu-id="47f49-103">Remove pontos de extremidade e metadados para se conectar a uma determinada instância do Azure.</span><span class="sxs-lookup"><span data-stu-id="47f49-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="47f49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47f49-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47f49-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="47f49-105">DESCRIPTION</span></span>
<span data-ttu-id="47f49-106">O cmdlet Remove-AzureRmEnvironment remove pontos de extremidade e informações de metadados para se conectar a uma determinada instância do Azure.</span><span class="sxs-lookup"><span data-stu-id="47f49-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="47f49-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47f49-107">EXAMPLES</span></span>

### <span data-ttu-id="47f49-108">Exemplo 1: Criando e removendo um ambiente de teste</span><span class="sxs-lookup"><span data-stu-id="47f49-108">Example 1: Creating and removing a test environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              : 
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : TestADEndpoint
GraphUrl                                          : TestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :

PS C:\> Remove-AzureRmEnvironment -Name TestEnvironment

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              : 
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : TestADEndpoint
GraphUrl                                          : TestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
```

<span data-ttu-id="47f49-109">Este exemplo mostra como criar um ambiente usando Add-AzureRmEnvironment e, em seguida, como excluir o ambiente usando Remove-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="47f49-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="47f49-110">OS</span><span class="sxs-lookup"><span data-stu-id="47f49-110">PARAMETERS</span></span>

### <span data-ttu-id="47f49-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="47f49-111">-Name</span></span>
<span data-ttu-id="47f49-112">Especifica o nome do ambiente a ser removido.</span><span class="sxs-lookup"><span data-stu-id="47f49-112">Specifies the name of the environment to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47f49-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="47f49-113">-Confirm</span></span>
<span data-ttu-id="47f49-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47f49-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47f49-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47f49-115">-WhatIf</span></span>
<span data-ttu-id="47f49-116">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="47f49-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47f49-117">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="47f49-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47f49-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47f49-118">CommonParameters</span></span>
<span data-ttu-id="47f49-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47f49-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47f49-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47f49-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47f49-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="47f49-121">INPUTS</span></span>

## <span data-ttu-id="47f49-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="47f49-122">OUTPUTS</span></span>

### <span data-ttu-id="47f49-123">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="47f49-123">PSAzureEnvironment</span></span>

## <span data-ttu-id="47f49-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="47f49-124">NOTES</span></span>

## <span data-ttu-id="47f49-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47f49-125">RELATED LINKS</span></span>

[<span data-ttu-id="47f49-126">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="47f49-126">Add-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="47f49-127">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="47f49-127">Get-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="47f49-128">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="47f49-128">Set-AzureRMEnvironment</span></span>]()

