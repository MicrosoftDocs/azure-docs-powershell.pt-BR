---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
ms.openlocfilehash: dcb9d6e58a743f37aa71d91b0b73772c239f252e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596785"
---
# <span data-ttu-id="8785c-101">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="8785c-101">Get-AzDataMigrationService</span></span>

## <span data-ttu-id="8785c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8785c-102">SYNOPSIS</span></span>
<span data-ttu-id="8785c-103">Recupera as propriedades associadas a uma instância do serviço de migração de banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="8785c-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

## <span data-ttu-id="8785c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8785c-104">SYNTAX</span></span>

### <span data-ttu-id="8785c-105">ResourceGroupSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8785c-105">ResourceGroupSet (Default)</span></span>
```
Get-AzDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8785c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8785c-106">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8785c-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="8785c-107">ServiceNameGroupSet</span></span>
```
Get-AzDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8785c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8785c-108">DESCRIPTION</span></span>
<span data-ttu-id="8785c-109">O cmdlet Get-AzDataMigrationService recupera as propriedades associadas a uma instância do serviço de migração de banco de dados do Azure com base no nome do serviço e no nome do grupo de recursos do Azure como parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="8785c-109">The Get-AzDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="8785c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8785c-110">EXAMPLES</span></span>

### <span data-ttu-id="8785c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8785c-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="8785c-112">O exemplo acima recupera as propriedades da instância do serviço de migração do banco de dados do Azure chamada testService.</span><span class="sxs-lookup"><span data-stu-id="8785c-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="8785c-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8785c-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup
```

<span data-ttu-id="8785c-114">O exemplo acima recupera os serviços de migração de banco de dados do Azure no grupo de recursos chamado testResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8785c-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="8785c-115">OS</span><span class="sxs-lookup"><span data-stu-id="8785c-115">PARAMETERS</span></span>

### <span data-ttu-id="8785c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8785c-116">-DefaultProfile</span></span>
<span data-ttu-id="8785c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8785c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8785c-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="8785c-118">-Name</span></span>
<span data-ttu-id="8785c-119">Nome do serviço de migração de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8785c-119">Name of Database Migration Service.</span></span>

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

### <span data-ttu-id="8785c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8785c-120">-ResourceGroupName</span></span>
<span data-ttu-id="8785c-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8785c-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="8785c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8785c-122">-ResourceId</span></span>
<span data-ttu-id="8785c-123">DataMigrationService ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="8785c-123">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="8785c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8785c-124">CommonParameters</span></span>
<span data-ttu-id="8785c-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8785c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8785c-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8785c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8785c-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8785c-127">INPUTS</span></span>

### <span data-ttu-id="8785c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8785c-128">System.String</span></span>

## <span data-ttu-id="8785c-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8785c-129">OUTPUTS</span></span>

### <span data-ttu-id="8785c-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="8785c-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="8785c-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8785c-131">NOTES</span></span>

## <span data-ttu-id="8785c-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8785c-132">RELATED LINKS</span></span>
