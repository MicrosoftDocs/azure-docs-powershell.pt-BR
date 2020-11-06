---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Get-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
ms.openlocfilehash: 06899e35e9119025aa13a310a3d6200c30b223df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431974"
---
# <span data-ttu-id="b101b-101">Get-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="b101b-101">Get-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="b101b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b101b-102">SYNOPSIS</span></span>
<span data-ttu-id="b101b-103">Recupera as propriedades associadas a uma instância do serviço de migração de banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="b101b-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b101b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b101b-104">SYNTAX</span></span>

### <span data-ttu-id="b101b-105">ResourceGroupSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b101b-105">ResourceGroupSet (Default)</span></span>
```
Get-AzureRmDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b101b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b101b-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b101b-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="b101b-107">ServiceNameGroupSet</span></span>
```
Get-AzureRmDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b101b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b101b-108">DESCRIPTION</span></span>
<span data-ttu-id="b101b-109">O cmdlet Get-AzureRmDataMigrationService recupera as propriedades associadas a uma instância do serviço de migração de banco de dados do Azure com base no nome do serviço e no nome do grupo de recursos do Azure como parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="b101b-109">The Get-AzureRmDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="b101b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b101b-110">EXAMPLES</span></span>

### <span data-ttu-id="b101b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b101b-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="b101b-112">O exemplo acima recupera as propriedades da instância do serviço de migração do banco de dados do Azure chamada testService.</span><span class="sxs-lookup"><span data-stu-id="b101b-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="b101b-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b101b-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup
```

<span data-ttu-id="b101b-114">O exemplo acima recupera os serviços de migração de banco de dados do Azure no grupo de recursos chamado testResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b101b-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="b101b-115">OS</span><span class="sxs-lookup"><span data-stu-id="b101b-115">PARAMETERS</span></span>

### <span data-ttu-id="b101b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b101b-116">-DefaultProfile</span></span>
<span data-ttu-id="b101b-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b101b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b101b-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="b101b-118">-Name</span></span>
<span data-ttu-id="b101b-119">Nome do serviço de migração de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b101b-119">Name of Database Migration Service.</span></span>

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

### <span data-ttu-id="b101b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b101b-120">-ResourceGroupName</span></span>
<span data-ttu-id="b101b-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b101b-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="b101b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b101b-122">-ResourceId</span></span>
<span data-ttu-id="b101b-123">DataMigrationService ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="b101b-123">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="b101b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b101b-124">CommonParameters</span></span>
<span data-ttu-id="b101b-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b101b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b101b-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b101b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b101b-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b101b-127">INPUTS</span></span>

### <span data-ttu-id="b101b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b101b-128">System.String</span></span>

## <span data-ttu-id="b101b-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b101b-129">OUTPUTS</span></span>

### <span data-ttu-id="b101b-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="b101b-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="b101b-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b101b-131">NOTES</span></span>

## <span data-ttu-id="b101b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b101b-132">RELATED LINKS</span></span>
