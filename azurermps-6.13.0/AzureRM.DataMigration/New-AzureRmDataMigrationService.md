---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
ms.openlocfilehash: cc2f708294be05b16b0c5be94fb9da260b479799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431969"
---
# <span data-ttu-id="913bb-101">New-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="913bb-101">New-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="913bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="913bb-102">SYNOPSIS</span></span>
<span data-ttu-id="913bb-103">Cria uma nova instância do serviço de migração de banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="913bb-103">Creates a new instance of the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="913bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="913bb-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> -Location <String> -Sku <String>
 -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="913bb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="913bb-105">DESCRIPTION</span></span>
<span data-ttu-id="913bb-106">O cmdlet New-AzureRmDataMigrationService cria uma nova instância do serviço de migração de banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="913bb-106">The New-AzureRmDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="913bb-107">Esse cmdlet usa o nome do grupo de recursos existente do Azure, o nome exclusivo da nova instância do serviço de migração de banco de dados do Azure a ser criada, a região em que a instância é provisionada, o nome da SKU do funcionário do DMS e o nome da sub-rede virtual do Azure em que o serviço está para residir.</span><span class="sxs-lookup"><span data-stu-id="913bb-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="913bb-108">Não há nenhum parâmetro para o nome da assinatura porque ele é esperado para o usuário especificar a assinatura padrão da sessão de logon do Azure ou executar Get-AzureRmSubscription-Subscriptionname "mysubscriptionname" | Select-AzureRmSubscription para selecionar outra assinatura.</span><span class="sxs-lookup"><span data-stu-id="913bb-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzureRmSubscription -SubscriptionName "MySubscription" | Select-AzureRmSubscription to select another subscription.</span></span>

## <span data-ttu-id="913bb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="913bb-109">EXAMPLES</span></span>

### <span data-ttu-id="913bb-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="913bb-110">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationService -ResourceGroupName myResourceGroup -Name TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="913bb-111">O exemplo acima mostra como criar uma nova instância do serviço de migração de banco de dados do Azure chamada TestService na região central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="913bb-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>

## <span data-ttu-id="913bb-112">OS</span><span class="sxs-lookup"><span data-stu-id="913bb-112">PARAMETERS</span></span>

### <span data-ttu-id="913bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="913bb-113">-DefaultProfile</span></span>
<span data-ttu-id="913bb-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="913bb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="913bb-115">-Local</span><span class="sxs-lookup"><span data-stu-id="913bb-115">-Location</span></span>
<span data-ttu-id="913bb-116">O local da instância do serviço de migração do banco de dados do Azure a ser criada, que corresponde a uma região do Azure.</span><span class="sxs-lookup"><span data-stu-id="913bb-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913bb-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="913bb-117">-Name</span></span>
<span data-ttu-id="913bb-118">Nome do serviço de migração de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="913bb-118">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913bb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="913bb-119">-ResourceGroupName</span></span>
<span data-ttu-id="913bb-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="913bb-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913bb-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="913bb-121">-Sku</span></span>
<span data-ttu-id="913bb-122">A SKU da instância do serviço de migração do banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="913bb-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="913bb-123">Atualmente, os valores possíveis são Basic_1vCore, Basic_2vCores GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="913bb-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913bb-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="913bb-124">-VirtualSubnetId</span></span>
<span data-ttu-id="913bb-125">O nome da sub-rede na rede virtual especificada a ser usada para a instância do serviço de migração do banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="913bb-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913bb-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="913bb-126">-Confirm</span></span>
<span data-ttu-id="913bb-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="913bb-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913bb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="913bb-128">-WhatIf</span></span>
<span data-ttu-id="913bb-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="913bb-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="913bb-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="913bb-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913bb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="913bb-131">CommonParameters</span></span>
<span data-ttu-id="913bb-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="913bb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="913bb-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="913bb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="913bb-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="913bb-134">INPUTS</span></span>

### <span data-ttu-id="913bb-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="913bb-135">None</span></span>

## <span data-ttu-id="913bb-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="913bb-136">OUTPUTS</span></span>

### <span data-ttu-id="913bb-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="913bb-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="913bb-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="913bb-138">NOTES</span></span>

## <span data-ttu-id="913bb-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="913bb-139">RELATED LINKS</span></span>
