---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Get-AzureRmDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
ms.openlocfilehash: 31d37f740500247fed433c3e40b9d8220a5af663
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431975"
---
# <span data-ttu-id="990ed-101">Get-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="990ed-101">Get-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="990ed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="990ed-102">SYNOPSIS</span></span>
<span data-ttu-id="990ed-103">Recupera as propriedades de um projeto de migração de banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="990ed-103">Retrieves the properties of an Azure Database Migration project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="990ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="990ed-104">SYNTAX</span></span>

### <span data-ttu-id="990ed-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="990ed-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="990ed-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="990ed-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="990ed-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="990ed-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="990ed-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="990ed-108">DESCRIPTION</span></span>
<span data-ttu-id="990ed-109">O cmdlet Get-AzureRmDataMigrationProject recupera as propriedades de um projeto de migração de banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="990ed-109">The Get-AzureRmDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="990ed-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="990ed-110">EXAMPLES</span></span>

### <span data-ttu-id="990ed-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="990ed-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="990ed-112">O exemplo acima recupera o projeto de migração do banco de dados do Azure chamado TestProject no grupo de recursos chamado testResourceGroup e em Service chamado testService</span><span class="sxs-lookup"><span data-stu-id="990ed-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="990ed-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="990ed-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -InputObject $myService
```

<span data-ttu-id="990ed-114">O exemplo acima recupera o projeto de migração do banco de dados do Azure com base no parâmetro de entrada do objeto PSProject passado.</span><span class="sxs-lookup"><span data-stu-id="990ed-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="990ed-115">OS</span><span class="sxs-lookup"><span data-stu-id="990ed-115">PARAMETERS</span></span>

### <span data-ttu-id="990ed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="990ed-116">-DefaultProfile</span></span>
<span data-ttu-id="990ed-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="990ed-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="990ed-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="990ed-118">-InputObject</span></span>
<span data-ttu-id="990ed-119">Objeto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="990ed-119">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="990ed-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="990ed-120">-Name</span></span>
<span data-ttu-id="990ed-121">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="990ed-121">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProjectName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="990ed-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="990ed-122">-ResourceGroupName</span></span>
<span data-ttu-id="990ed-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="990ed-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="990ed-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="990ed-124">-ResourceId</span></span>
<span data-ttu-id="990ed-125">DataMigrationService ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="990ed-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="990ed-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="990ed-126">-ServiceName</span></span>
<span data-ttu-id="990ed-127">Nome do serviço de migração de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="990ed-127">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="990ed-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="990ed-128">CommonParameters</span></span>
<span data-ttu-id="990ed-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="990ed-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="990ed-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="990ed-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="990ed-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="990ed-131">INPUTS</span></span>

### <span data-ttu-id="990ed-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="990ed-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="990ed-133">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="990ed-133">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="990ed-134">System. String</span><span class="sxs-lookup"><span data-stu-id="990ed-134">System.String</span></span>

## <span data-ttu-id="990ed-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="990ed-135">OUTPUTS</span></span>

### <span data-ttu-id="990ed-136">Microsoft. Azure. Commands. datamigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="990ed-136">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="990ed-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="990ed-137">NOTES</span></span>

## <span data-ttu-id="990ed-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="990ed-138">RELATED LINKS</span></span>
