---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Get-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
ms.openlocfilehash: 4dfe4f52a344b8d2308288cfb659792c7b4aabab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886227"
---
# <span data-ttu-id="6f472-101">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="6f472-101">Get-AzDataMigrationService</span></span>

## <span data-ttu-id="6f472-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f472-102">SYNOPSIS</span></span>
<span data-ttu-id="6f472-103">Recupera as propriedades associadas a uma instância do Serviço de Migração de Banco de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="6f472-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

## <span data-ttu-id="6f472-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6f472-104">SYNTAX</span></span>

### <span data-ttu-id="6f472-105">ResourceGroupSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6f472-105">ResourceGroupSet (Default)</span></span>
```
Get-AzDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6f472-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f472-106">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6f472-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="6f472-107">ServiceNameGroupSet</span></span>
```
Get-AzDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f472-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6f472-108">DESCRIPTION</span></span>
<span data-ttu-id="6f472-109">O Get-AzDataMigrationService cmdlet recupera as propriedades associadas a uma instância do Serviço de Migração de Banco de Dados do Azure com base no nome do serviço e no nome do Grupo de Recursos do Azure como parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="6f472-109">The Get-AzDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="6f472-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6f472-110">EXAMPLES</span></span>

### <span data-ttu-id="6f472-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6f472-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="6f472-112">O exemplo acima recupera as propriedades da instância do Serviço de Migração de Banco de Dados do Azure chamada testService.</span><span class="sxs-lookup"><span data-stu-id="6f472-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="6f472-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6f472-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup
```

<span data-ttu-id="6f472-114">O exemplo acima recupera os Serviços de Migração de Banco de Dados do Azure no grupo de recursos chamado testResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6f472-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="6f472-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6f472-115">PARAMETERS</span></span>

### <span data-ttu-id="6f472-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f472-116">-DefaultProfile</span></span>
<span data-ttu-id="6f472-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6f472-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f472-118">-Name</span><span class="sxs-lookup"><span data-stu-id="6f472-118">-Name</span></span>
<span data-ttu-id="6f472-119">Nome do Serviço de Migração de Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="6f472-119">Name of Database Migration Service.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f472-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f472-120">-ResourceGroupName</span></span>
<span data-ttu-id="6f472-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6f472-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f472-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f472-122">-ResourceId</span></span>
<span data-ttu-id="6f472-123">ID do Recurso DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="6f472-123">DataMigrationService Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f472-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f472-124">CommonParameters</span></span>
<span data-ttu-id="6f472-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f472-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f472-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f472-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f472-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f472-127">INPUTS</span></span>

### <span data-ttu-id="6f472-128">System.String</span><span class="sxs-lookup"><span data-stu-id="6f472-128">System.String</span></span>

## <span data-ttu-id="6f472-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6f472-129">OUTPUTS</span></span>

### <span data-ttu-id="6f472-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="6f472-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="6f472-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="6f472-131">NOTES</span></span>

## <span data-ttu-id="6f472-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f472-132">RELATED LINKS</span></span>
