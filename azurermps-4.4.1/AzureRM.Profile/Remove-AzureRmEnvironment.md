---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
ms.openlocfilehash: d27a05e652cbcd11d35536ebff97f04b3c60f520
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610744"
---
# <span data-ttu-id="44435-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="44435-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="44435-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44435-102">SYNOPSIS</span></span>
<span data-ttu-id="44435-103">Remove pontos de extremidade e metadados para se conectar a uma determinada instância do Azure.</span><span class="sxs-lookup"><span data-stu-id="44435-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44435-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44435-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44435-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="44435-105">DESCRIPTION</span></span>
<span data-ttu-id="44435-106">O cmdlet Remove-AzureRmEnvironment remove pontos de extremidade e informações de metadados para se conectar a uma determinada instância do Azure.</span><span class="sxs-lookup"><span data-stu-id="44435-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="44435-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44435-107">EXAMPLES</span></span>

### <span data-ttu-id="44435-108">Exemplo 1: Criando e removendo um ambiente de teste</span><span class="sxs-lookup"><span data-stu-id="44435-108">Example 1: Creating and removing a test environment</span></span>
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

<span data-ttu-id="44435-109">Este exemplo mostra como criar um ambiente usando Add-AzureRmEnvironment e, em seguida, como excluir o ambiente usando Remove-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="44435-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="44435-110">OS</span><span class="sxs-lookup"><span data-stu-id="44435-110">PARAMETERS</span></span>

### <span data-ttu-id="44435-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44435-111">-DefaultProfile</span></span>
<span data-ttu-id="44435-112">As credenciais, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44435-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44435-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="44435-113">-Name</span></span>
<span data-ttu-id="44435-114">Especifica o nome do ambiente a ser removido.</span><span class="sxs-lookup"><span data-stu-id="44435-114">Specifies the name of the environment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44435-115">-Escopo</span><span class="sxs-lookup"><span data-stu-id="44435-115">-Scope</span></span>
<span data-ttu-id="44435-116">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="44435-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44435-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="44435-117">-Confirm</span></span>
<span data-ttu-id="44435-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44435-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44435-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44435-119">-WhatIf</span></span>
<span data-ttu-id="44435-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="44435-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44435-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44435-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44435-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44435-122">CommonParameters</span></span>
<span data-ttu-id="44435-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44435-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44435-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44435-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44435-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="44435-125">INPUTS</span></span>

## <span data-ttu-id="44435-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="44435-126">OUTPUTS</span></span>

### <span data-ttu-id="44435-127">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="44435-127">PSAzureEnvironment</span></span>

## <span data-ttu-id="44435-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="44435-128">NOTES</span></span>

## <span data-ttu-id="44435-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44435-129">RELATED LINKS</span></span>

[<span data-ttu-id="44435-130">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="44435-130">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="44435-131">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="44435-131">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="44435-132">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="44435-132">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

