---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
ms.openlocfilehash: cac57ff34d925d553c25d97facd81dba017a25c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431682"
---
# <span data-ttu-id="2d71e-101">Get-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="2d71e-101">Get-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="2d71e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2d71e-102">SYNOPSIS</span></span>
<span data-ttu-id="2d71e-103">Recupera as propriedades associadas a uma instância do serviço de migração de banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="2d71e-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d71e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d71e-104">SYNTAX</span></span>

### <span data-ttu-id="2d71e-105">ResourceGroupSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2d71e-105">ResourceGroupSet (Default)</span></span>
```
Get-AzureRmDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="2d71e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d71e-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="2d71e-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="2d71e-107">ServiceNameGroupSet</span></span>
```
Get-AzureRmDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>]
```
## <span data-ttu-id="2d71e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2d71e-108">DESCRIPTION</span></span>
<span data-ttu-id="2d71e-109">O cmdlet Get-AzureRmDataMigrationService recupera as propriedades associadas a uma instância do serviço de migração de banco de dados do Azure com base no nome do serviço e no nome do grupo de recursos do Azure como parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="2d71e-109">The Get-AzureRmDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="2d71e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2d71e-110">EXAMPLES</span></span>

### <span data-ttu-id="2d71e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2d71e-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="2d71e-112">O exemplo acima recupera as propriedades da instância do serviço de migração do banco de dados do Azure chamada testService.</span><span class="sxs-lookup"><span data-stu-id="2d71e-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="2d71e-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2d71e-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup 
```

<span data-ttu-id="2d71e-114">O exemplo acima recupera os serviços de migração de banco de dados do Azure no grupo de recursos chamado testResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2d71e-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="2d71e-115">OS</span><span class="sxs-lookup"><span data-stu-id="2d71e-115">PARAMETERS</span></span>

### <span data-ttu-id="2d71e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d71e-116">-DefaultProfile</span></span>
<span data-ttu-id="2d71e-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d71e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d71e-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="2d71e-118">-Name</span></span>
<span data-ttu-id="2d71e-119">Nome do serviço de migração de dados.</span><span class="sxs-lookup"><span data-stu-id="2d71e-119">Name of Data Migration Service.</span></span>

```yaml
Type: String
Parameter Sets: ServiceNameGroupSet
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d71e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d71e-120">-ResourceGroupName</span></span>
<span data-ttu-id="2d71e-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2d71e-121">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServiceNameGroupSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d71e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d71e-122">-ResourceId</span></span>
<span data-ttu-id="2d71e-123">DataMigrationService ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="2d71e-123">DataMigrationService Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="2d71e-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2d71e-124">INPUTS</span></span>

### <span data-ttu-id="2d71e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2d71e-125">System.String</span></span>


## <span data-ttu-id="2d71e-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2d71e-126">OUTPUTS</span></span>

### <span data-ttu-id="2d71e-127">System. Collections. Generic. IList ' 1 [[Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService, Microsoft. Azure. Commands. datamigration, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2d71e-127">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService, Microsoft.Azure.Commands.DataMigration, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="2d71e-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2d71e-128">NOTES</span></span>

## <span data-ttu-id="2d71e-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d71e-129">RELATED LINKS</span></span>





