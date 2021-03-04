---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Get-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
ms.openlocfilehash: 5485693da87dbbb49b5e06e221e818de9bd222d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891032"
---
# <span data-ttu-id="743de-101">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="743de-101">Get-AzDataMigrationProject</span></span>

## <span data-ttu-id="743de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="743de-102">SYNOPSIS</span></span>
<span data-ttu-id="743de-103">Recupera as propriedades de um projeto de Migração de Banco de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="743de-103">Retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="743de-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="743de-104">SYNTAX</span></span>

### <span data-ttu-id="743de-105">ComponentNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="743de-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="743de-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="743de-106">ComponentObjectParameterSet</span></span>
```
Get-AzDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="743de-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="743de-107">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationProject [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="743de-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="743de-108">DESCRIPTION</span></span>
<span data-ttu-id="743de-109">O Get-AzDataMigrationProject cmdlet recupera as propriedades de um projeto de Migração de Banco de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="743de-109">The Get-AzDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="743de-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="743de-110">EXAMPLES</span></span>

### <span data-ttu-id="743de-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="743de-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="743de-112">O exemplo acima recupera o projeto de Migração de Banco de Dados do Azure chamado TestProject no grupo de recursos chamado testResourceGroup e em serviço chamado testService</span><span class="sxs-lookup"><span data-stu-id="743de-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="743de-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="743de-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationProject -InputObject $myService
```

<span data-ttu-id="743de-114">O exemplo acima recupera o projeto de Migração de Banco de Dados do Azure com base no parâmetro de entrada de objeto PSProject passado.</span><span class="sxs-lookup"><span data-stu-id="743de-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="743de-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="743de-115">PARAMETERS</span></span>

### <span data-ttu-id="743de-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="743de-116">-DefaultProfile</span></span>
<span data-ttu-id="743de-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="743de-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="743de-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="743de-118">-InputObject</span></span>
<span data-ttu-id="743de-119">Objeto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="743de-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="743de-120">-Name</span><span class="sxs-lookup"><span data-stu-id="743de-120">-Name</span></span>
<span data-ttu-id="743de-121">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="743de-121">The name of the project.</span></span>

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

### <span data-ttu-id="743de-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="743de-122">-ResourceGroupName</span></span>
<span data-ttu-id="743de-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="743de-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="743de-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="743de-124">-ResourceId</span></span>
<span data-ttu-id="743de-125">ID do Recurso DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="743de-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="743de-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="743de-126">-ServiceName</span></span>
<span data-ttu-id="743de-127">Nome do Serviço de Migração de Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="743de-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="743de-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="743de-128">CommonParameters</span></span>
<span data-ttu-id="743de-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="743de-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="743de-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="743de-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="743de-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="743de-131">INPUTS</span></span>

### <span data-ttu-id="743de-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="743de-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="743de-133">System.String</span><span class="sxs-lookup"><span data-stu-id="743de-133">System.String</span></span>

## <span data-ttu-id="743de-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="743de-134">OUTPUTS</span></span>

### <span data-ttu-id="743de-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="743de-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="743de-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="743de-136">NOTES</span></span>

## <span data-ttu-id="743de-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="743de-137">RELATED LINKS</span></span>
