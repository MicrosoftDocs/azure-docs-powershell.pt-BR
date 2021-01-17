---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
ms.openlocfilehash: 7fe1e12c7c7feb2a47ac33b309b188e53e77fc73
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426577"
---
# <span data-ttu-id="2e1b0-101">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="2e1b0-101">Get-AzDataMigrationProject</span></span>

## <span data-ttu-id="2e1b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e1b0-102">SYNOPSIS</span></span>
<span data-ttu-id="2e1b0-103">Recupera as propriedades de um projeto de migração de banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-103">Retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="2e1b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e1b0-104">SYNTAX</span></span>

### <span data-ttu-id="2e1b0-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2e1b0-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e1b0-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e1b0-106">ComponentObjectParameterSet</span></span>
```
Get-AzDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e1b0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e1b0-107">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationProject [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e1b0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e1b0-108">DESCRIPTION</span></span>
<span data-ttu-id="2e1b0-109">O cmdlet Get-AzDataMigrationProject recupera as propriedades de um projeto de migração de banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-109">The Get-AzDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="2e1b0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e1b0-110">EXAMPLES</span></span>

### <span data-ttu-id="2e1b0-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2e1b0-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="2e1b0-112">O exemplo acima recupera o projeto de migração do banco de dados do Azure chamado TestProject no grupo de recursos chamado testResourceGroup e em Service chamado testService</span><span class="sxs-lookup"><span data-stu-id="2e1b0-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="2e1b0-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2e1b0-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationProject -InputObject $myService
```

<span data-ttu-id="2e1b0-114">O exemplo acima recupera o projeto de migração do banco de dados do Azure com base no parâmetro de entrada do objeto PSProject passado.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="2e1b0-115">OS</span><span class="sxs-lookup"><span data-stu-id="2e1b0-115">PARAMETERS</span></span>

### <span data-ttu-id="2e1b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e1b0-116">-DefaultProfile</span></span>
<span data-ttu-id="2e1b0-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e1b0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e1b0-118">-InputObject</span></span>
<span data-ttu-id="2e1b0-119">Objeto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="2e1b0-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e1b0-120">-Name</span></span>
<span data-ttu-id="2e1b0-121">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-121">The name of the project.</span></span>

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

### <span data-ttu-id="2e1b0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e1b0-122">-ResourceGroupName</span></span>
<span data-ttu-id="2e1b0-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="2e1b0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e1b0-124">-ResourceId</span></span>
<span data-ttu-id="2e1b0-125">DataMigrationService ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="2e1b0-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2e1b0-126">-ServiceName</span></span>
<span data-ttu-id="2e1b0-127">Nome do serviço de migração de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="2e1b0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e1b0-128">CommonParameters</span></span>
<span data-ttu-id="2e1b0-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e1b0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e1b0-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e1b0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e1b0-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e1b0-131">INPUTS</span></span>

### <span data-ttu-id="2e1b0-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="2e1b0-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="2e1b0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2e1b0-133">System.String</span></span>

## <span data-ttu-id="2e1b0-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e1b0-134">OUTPUTS</span></span>

### <span data-ttu-id="2e1b0-135">Microsoft. Azure. Commands. datamigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="2e1b0-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="2e1b0-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e1b0-136">NOTES</span></span>

## <span data-ttu-id="2e1b0-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e1b0-137">RELATED LINKS</span></span>
