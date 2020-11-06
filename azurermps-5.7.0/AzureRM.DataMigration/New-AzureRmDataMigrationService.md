---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
ms.openlocfilehash: 46455cbf411228f008bdc15c27f78715ccea0e89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610399"
---
# <span data-ttu-id="01760-101">New-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="01760-101">New-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="01760-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="01760-102">SYNOPSIS</span></span>
<span data-ttu-id="01760-103">Cria uma nova instância do serviço de migração de banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="01760-103">Creates a new instance of the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01760-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01760-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationService -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Sku <String> -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="01760-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="01760-105">DESCRIPTION</span></span>
<span data-ttu-id="01760-106">O cmdlet New-AzureRmDataMigrationService cria uma nova instância do serviço de migração de banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="01760-106">The New-AzureRmDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="01760-107">Esse cmdlet usa o nome do grupo de recursos existente do Azure, o nome exclusivo da nova instância do serviço de migração de banco de dados do Azure a ser criada, a região em que a instância é provisionada, o nome da SKU do funcionário do DMS e o nome da sub-rede virtual do Azure em que o serviço está para residir.</span><span class="sxs-lookup"><span data-stu-id="01760-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="01760-108">Não há nenhum parâmetro para o nome da assinatura porque ele é esperado para que o usuário especifique a assinatura padrão da sessão de logon do Azure ou execute Get-AzureRmSubscription-Subscriptionname "mysubscriptionname" | Select-AzureRmSubscription para selecionar outra assinatura.</span><span class="sxs-lookup"><span data-stu-id="01760-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzureRmSubscription –SubscriptionName "MySubscription" | Select-AzureRmSubscription to select another subscription.</span></span>

## <span data-ttu-id="01760-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="01760-109">EXAMPLES</span></span>

### <span data-ttu-id="01760-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="01760-110">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationService -ResourceGroupName myResourceGroup -ServiceName TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="01760-111">O exemplo acima mostra como criar uma nova instância do serviço de migração de banco de dados do Azure chamada TestService na região central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="01760-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>


## <span data-ttu-id="01760-112">OS</span><span class="sxs-lookup"><span data-stu-id="01760-112">PARAMETERS</span></span>

### <span data-ttu-id="01760-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01760-113">-DefaultProfile</span></span>
<span data-ttu-id="01760-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="01760-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01760-115">-Local</span><span class="sxs-lookup"><span data-stu-id="01760-115">-Location</span></span>
<span data-ttu-id="01760-116">O local da instância do serviço de migração do banco de dados do Azure a ser criada, que corresponde a uma região do Azure.</span><span class="sxs-lookup"><span data-stu-id="01760-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01760-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01760-117">-ResourceGroupName</span></span>
<span data-ttu-id="01760-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="01760-118">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01760-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="01760-119">-ServiceName</span></span>
<span data-ttu-id="01760-120">O nome da instância do serviço de migração do banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="01760-120">The name of the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01760-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="01760-121">-Sku</span></span>
<span data-ttu-id="01760-122">A SKU da instância do serviço de migração do banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="01760-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="01760-123">Atualmente, os valores possíveis são Basic_1vCore, Basic_2vCores GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="01760-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01760-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="01760-124">-VirtualSubnetId</span></span>
<span data-ttu-id="01760-125">O nome da sub-rede na rede virtual especificada a ser usada para a instância do serviço de migração do banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="01760-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```




## <span data-ttu-id="01760-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="01760-126">OUTPUTS</span></span>

### <span data-ttu-id="01760-127">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="01760-127">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>


## <span data-ttu-id="01760-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="01760-128">NOTES</span></span>

## <span data-ttu-id="01760-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01760-129">RELATED LINKS</span></span>

