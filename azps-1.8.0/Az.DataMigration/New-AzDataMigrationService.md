---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
ms.openlocfilehash: b3978bcc0e3b883d95c5161ca1b24f9cd6c6c1f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770892"
---
# <span data-ttu-id="ff68c-101">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="ff68c-101">New-AzDataMigrationService</span></span>

## <span data-ttu-id="ff68c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff68c-102">SYNOPSIS</span></span>
<span data-ttu-id="ff68c-103">Cria uma nova instância do serviço de migração de banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="ff68c-103">Creates a new instance of the Azure Database Migration Service.</span></span>

## <span data-ttu-id="ff68c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff68c-104">SYNTAX</span></span>

```
New-AzDataMigrationService -ResourceGroupName <String> -Name <String> -Location <String> -Sku <String>
 -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff68c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ff68c-105">DESCRIPTION</span></span>
<span data-ttu-id="ff68c-106">O cmdlet New-AzDataMigrationService cria uma nova instância do serviço de migração de banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="ff68c-106">The New-AzDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="ff68c-107">Esse cmdlet usa o nome do grupo de recursos existente do Azure, o nome exclusivo da nova instância do serviço de migração de banco de dados do Azure a ser criada, a região em que a instância é provisionada, o nome da SKU do funcionário do DMS e o nome da sub-rede virtual do Azure em que o serviço está para residir.</span><span class="sxs-lookup"><span data-stu-id="ff68c-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="ff68c-108">Não há nenhum parâmetro para o nome da assinatura porque ele é esperado para o usuário especificar a assinatura padrão da sessão de logon do Azure ou executar Get-AzSubscription-Subscriptionname "mysubscriptionname" | Select-AzSubscription para selecionar outra assinatura.</span><span class="sxs-lookup"><span data-stu-id="ff68c-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzSubscription -SubscriptionName "MySubscription" | Select-AzSubscription to select another subscription.</span></span>

## <span data-ttu-id="ff68c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff68c-109">EXAMPLES</span></span>

### <span data-ttu-id="ff68c-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ff68c-110">Example 1</span></span>
```
PS C:\> New-AzDataMigrationService -ResourceGroupName myResourceGroup -Name TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="ff68c-111">O exemplo acima mostra como criar uma nova instância do serviço de migração de banco de dados do Azure chamada TestService na região central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="ff68c-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>

## <span data-ttu-id="ff68c-112">OS</span><span class="sxs-lookup"><span data-stu-id="ff68c-112">PARAMETERS</span></span>

### <span data-ttu-id="ff68c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff68c-113">-DefaultProfile</span></span>
<span data-ttu-id="ff68c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ff68c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff68c-115">-Local</span><span class="sxs-lookup"><span data-stu-id="ff68c-115">-Location</span></span>
<span data-ttu-id="ff68c-116">O local da instância do serviço de migração do banco de dados do Azure a ser criada, que corresponde a uma região do Azure.</span><span class="sxs-lookup"><span data-stu-id="ff68c-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

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

### <span data-ttu-id="ff68c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff68c-117">-Name</span></span>
<span data-ttu-id="ff68c-118">Nome do serviço de migração de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ff68c-118">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="ff68c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff68c-119">-ResourceGroupName</span></span>
<span data-ttu-id="ff68c-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ff68c-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="ff68c-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="ff68c-121">-Sku</span></span>
<span data-ttu-id="ff68c-122">A SKU da instância do serviço de migração do banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="ff68c-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="ff68c-123">Atualmente, os valores possíveis são Basic_1vCore, Basic_2vCores GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="ff68c-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

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

### <span data-ttu-id="ff68c-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="ff68c-124">-VirtualSubnetId</span></span>
<span data-ttu-id="ff68c-125">O nome da sub-rede na rede virtual especificada a ser usada para a instância do serviço de migração do banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="ff68c-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="ff68c-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ff68c-126">-Confirm</span></span>
<span data-ttu-id="ff68c-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff68c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff68c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff68c-128">-WhatIf</span></span>
<span data-ttu-id="ff68c-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ff68c-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff68c-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ff68c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff68c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff68c-131">CommonParameters</span></span>
<span data-ttu-id="ff68c-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff68c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff68c-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff68c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff68c-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ff68c-134">INPUTS</span></span>

### <span data-ttu-id="ff68c-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ff68c-135">None</span></span>

## <span data-ttu-id="ff68c-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ff68c-136">OUTPUTS</span></span>

### <span data-ttu-id="ff68c-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="ff68c-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="ff68c-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ff68c-138">NOTES</span></span>

## <span data-ttu-id="ff68c-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff68c-139">RELATED LINKS</span></span>
