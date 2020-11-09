---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
ms.openlocfilehash: 7fe1e12c7c7feb2a47ac33b309b188e53e77fc73
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280782"
---
# <span data-ttu-id="0bd61-101">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="0bd61-101">Get-AzDataMigrationProject</span></span>

## <span data-ttu-id="0bd61-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0bd61-102">SYNOPSIS</span></span>
<span data-ttu-id="0bd61-103">Recupera as propriedades de um projeto de migração de banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="0bd61-103">Retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="0bd61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0bd61-104">SYNTAX</span></span>

### <span data-ttu-id="0bd61-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0bd61-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bd61-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bd61-106">ComponentObjectParameterSet</span></span>
```
Get-AzDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bd61-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bd61-107">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationProject [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0bd61-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0bd61-108">DESCRIPTION</span></span>
<span data-ttu-id="0bd61-109">O cmdlet Get-AzDataMigrationProject recupera as propriedades de um projeto de migração de banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="0bd61-109">The Get-AzDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="0bd61-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0bd61-110">EXAMPLES</span></span>

### <span data-ttu-id="0bd61-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0bd61-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="0bd61-112">O exemplo acima recupera o projeto de migração do banco de dados do Azure chamado TestProject no grupo de recursos chamado testResourceGroup e em Service chamado testService</span><span class="sxs-lookup"><span data-stu-id="0bd61-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="0bd61-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0bd61-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationProject -InputObject $myService
```

<span data-ttu-id="0bd61-114">O exemplo acima recupera o projeto de migração do banco de dados do Azure com base no parâmetro de entrada do objeto PSProject passado.</span><span class="sxs-lookup"><span data-stu-id="0bd61-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="0bd61-115">OS</span><span class="sxs-lookup"><span data-stu-id="0bd61-115">PARAMETERS</span></span>

### <span data-ttu-id="0bd61-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bd61-116">-DefaultProfile</span></span>
<span data-ttu-id="0bd61-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0bd61-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bd61-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0bd61-118">-InputObject</span></span>
<span data-ttu-id="0bd61-119">Objeto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="0bd61-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="0bd61-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="0bd61-120">-Name</span></span>
<span data-ttu-id="0bd61-121">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="0bd61-121">The name of the project.</span></span>

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

### <span data-ttu-id="0bd61-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bd61-122">-ResourceGroupName</span></span>
<span data-ttu-id="0bd61-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0bd61-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="0bd61-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bd61-124">-ResourceId</span></span>
<span data-ttu-id="0bd61-125">DataMigrationService ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="0bd61-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="0bd61-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0bd61-126">-ServiceName</span></span>
<span data-ttu-id="0bd61-127">Nome do serviço de migração de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0bd61-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="0bd61-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bd61-128">CommonParameters</span></span>
<span data-ttu-id="0bd61-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bd61-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bd61-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bd61-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bd61-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0bd61-131">INPUTS</span></span>

### <span data-ttu-id="0bd61-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="0bd61-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="0bd61-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0bd61-133">System.String</span></span>

## <span data-ttu-id="0bd61-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0bd61-134">OUTPUTS</span></span>

### <span data-ttu-id="0bd61-135">Microsoft. Azure. Commands. datamigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="0bd61-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="0bd61-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0bd61-136">NOTES</span></span>

## <span data-ttu-id="0bd61-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0bd61-137">RELATED LINKS</span></span>
