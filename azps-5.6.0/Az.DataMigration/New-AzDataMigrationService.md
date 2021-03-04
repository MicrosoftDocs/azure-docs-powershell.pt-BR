---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
ms.openlocfilehash: 7d36860991d5b6b12fb23044cc607044fb87bfa6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892979"
---
# <span data-ttu-id="51081-101">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="51081-101">New-AzDataMigrationService</span></span>

## <span data-ttu-id="51081-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51081-102">SYNOPSIS</span></span>
<span data-ttu-id="51081-103">Cria uma nova instância do Serviço de Migração de Banco de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="51081-103">Creates a new instance of the Azure Database Migration Service.</span></span>

## <span data-ttu-id="51081-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="51081-104">SYNTAX</span></span>

```
New-AzDataMigrationService -ResourceGroupName <String> -Name <String> -Location <String> -Sku <String>
 -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51081-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="51081-105">DESCRIPTION</span></span>
<span data-ttu-id="51081-106">O New-AzDataMigrationService cmdlet cria uma nova instância do Serviço de Migração de Banco de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="51081-106">The New-AzDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="51081-107">Este cmdlet leva em nome do Grupo de Recursos do Azure existente, o nome exclusivo para a nova instância do Serviço de Migração de Banco de Dados do Azure a ser criado, a região na qual a instância é provisionada, o nome da SKU de Trabalho do DMS e o nome da Sub-rede Virtual do Azure na qual o serviço deve residir.</span><span class="sxs-lookup"><span data-stu-id="51081-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="51081-108">Não há parâmetro para o nome da assinatura, pois é esperado que o usuário especifique a assinatura padrão da sessão de logon do Azure ou execute o Get-AzSubscription -SubscriptionName "MySubscription" | Select-AzSubscription selecionar outra assinatura.</span><span class="sxs-lookup"><span data-stu-id="51081-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzSubscription -SubscriptionName "MySubscription" | Select-AzSubscription to select another subscription.</span></span>

## <span data-ttu-id="51081-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51081-109">EXAMPLES</span></span>

### <span data-ttu-id="51081-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="51081-110">Example 1</span></span>
```
PS C:\> New-AzDataMigrationService -ResourceGroupName myResourceGroup -Name TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="51081-111">O exemplo acima mostra como criar uma nova instância do Serviço de Migração de Banco de Dados do Azure chamado TestService na região central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="51081-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>

## <span data-ttu-id="51081-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="51081-112">PARAMETERS</span></span>

### <span data-ttu-id="51081-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51081-113">-DefaultProfile</span></span>
<span data-ttu-id="51081-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="51081-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51081-115">-Location</span><span class="sxs-lookup"><span data-stu-id="51081-115">-Location</span></span>
<span data-ttu-id="51081-116">O local da instância do Serviço de Migração de Banco de Dados do Azure a ser criado, que corresponde a uma região do Azure.</span><span class="sxs-lookup"><span data-stu-id="51081-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

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

### <span data-ttu-id="51081-117">-Name</span><span class="sxs-lookup"><span data-stu-id="51081-117">-Name</span></span>
<span data-ttu-id="51081-118">Nome do Serviço de Migração de Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="51081-118">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="51081-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51081-119">-ResourceGroupName</span></span>
<span data-ttu-id="51081-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="51081-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="51081-121">-Sku</span><span class="sxs-lookup"><span data-stu-id="51081-121">-Sku</span></span>
<span data-ttu-id="51081-122">O sku da instância do Serviço de Migração de Banco de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="51081-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="51081-123">Os valores possíveis atualmente são Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="51081-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

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

### <span data-ttu-id="51081-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="51081-124">-VirtualSubnetId</span></span>
<span data-ttu-id="51081-125">O nome da sub-rede na rede virtual especificada a ser usada para a instância do Serviço de Migração de Banco de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="51081-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="51081-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51081-126">-Confirm</span></span>
<span data-ttu-id="51081-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51081-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51081-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51081-128">-WhatIf</span></span>
<span data-ttu-id="51081-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="51081-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51081-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="51081-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51081-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51081-131">CommonParameters</span></span>
<span data-ttu-id="51081-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51081-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51081-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51081-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51081-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="51081-134">INPUTS</span></span>

### <span data-ttu-id="51081-135">Nenhum</span><span class="sxs-lookup"><span data-stu-id="51081-135">None</span></span>

## <span data-ttu-id="51081-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="51081-136">OUTPUTS</span></span>

### <span data-ttu-id="51081-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="51081-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="51081-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="51081-138">NOTES</span></span>

## <span data-ttu-id="51081-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51081-139">RELATED LINKS</span></span>
