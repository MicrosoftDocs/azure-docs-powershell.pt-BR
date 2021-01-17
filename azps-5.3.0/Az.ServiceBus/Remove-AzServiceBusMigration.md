---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
ms.openlocfilehash: 42bb6a61e2298c43cb0828a031495b086b46c9d2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433121"
---
# <span data-ttu-id="9da07-101">Remove-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="9da07-101">Remove-AzServiceBusMigration</span></span>

## <span data-ttu-id="9da07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9da07-102">SYNOPSIS</span></span>
<span data-ttu-id="9da07-103">Cmdlet exclui a configuração de migração de namespaces padrão para Premium</span><span class="sxs-lookup"><span data-stu-id="9da07-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="9da07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9da07-104">SYNTAX</span></span>

### <span data-ttu-id="9da07-105">MigrationConfigurationPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9da07-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9da07-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9da07-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9da07-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9da07-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9da07-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9da07-108">DESCRIPTION</span></span>
<span data-ttu-id="9da07-109">O cmdlet **Remove-AzServiceBusMigration** exclui a configuração de migração para namespaces padrão para Premium</span><span class="sxs-lookup"><span data-stu-id="9da07-109">The **Remove-AzServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="9da07-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9da07-110">EXAMPLES</span></span>

### <span data-ttu-id="9da07-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9da07-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="9da07-112">Exclui a configuração de migração ' TestingNamespaceStandardMigration '</span><span class="sxs-lookup"><span data-stu-id="9da07-112">Deletes the 'TestingNamespaceStandardMigration' migration configuration</span></span>

## <span data-ttu-id="9da07-113">OS</span><span class="sxs-lookup"><span data-stu-id="9da07-113">PARAMETERS</span></span>

### <span data-ttu-id="9da07-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9da07-114">-AsJob</span></span>
<span data-ttu-id="9da07-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9da07-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9da07-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9da07-116">-DefaultProfile</span></span>
<span data-ttu-id="9da07-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9da07-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9da07-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9da07-118">-InputObject</span></span>
<span data-ttu-id="9da07-119">Objeto namespace padrão de migração do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="9da07-119">Service Bus Migration Standard Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9da07-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="9da07-120">-Name</span></span>
<span data-ttu-id="9da07-121">Nome do namespace padrão</span><span class="sxs-lookup"><span data-stu-id="9da07-121">Standard Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9da07-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9da07-122">-PassThru</span></span>
<span data-ttu-id="9da07-123">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="9da07-123">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9da07-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9da07-124">-ResourceGroupName</span></span>
<span data-ttu-id="9da07-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9da07-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9da07-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9da07-126">-ResourceId</span></span>
<span data-ttu-id="9da07-127">ID do recurso namespace padrão da migração do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="9da07-127">Service Bus Migration Standard Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9da07-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9da07-128">-Confirm</span></span>
<span data-ttu-id="9da07-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9da07-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9da07-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9da07-130">-WhatIf</span></span>
<span data-ttu-id="9da07-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9da07-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9da07-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9da07-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9da07-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9da07-133">CommonParameters</span></span>
<span data-ttu-id="9da07-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9da07-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9da07-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9da07-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9da07-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9da07-136">INPUTS</span></span>

### <span data-ttu-id="9da07-137">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="9da07-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="9da07-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9da07-138">System.String</span></span>

## <span data-ttu-id="9da07-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9da07-139">OUTPUTS</span></span>

### <span data-ttu-id="9da07-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9da07-140">System.Boolean</span></span>

## <span data-ttu-id="9da07-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9da07-141">NOTES</span></span>

## <span data-ttu-id="9da07-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9da07-142">RELATED LINKS</span></span>
