---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/stop-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
ms.openlocfilehash: fc0cc8acf45403593124135cab87072a719f291d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886586"
---
# <span data-ttu-id="582bd-101">Stop-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="582bd-101">Stop-AzServiceBusMigration</span></span>

## <span data-ttu-id="582bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="582bd-102">SYNOPSIS</span></span>
<span data-ttu-id="582bd-103">{{Preencha o Synopsis}}</span><span class="sxs-lookup"><span data-stu-id="582bd-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="582bd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="582bd-104">SYNTAX</span></span>

### <span data-ttu-id="582bd-105">MigrationConfigurationPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="582bd-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="582bd-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="582bd-106">NamespaceInputObjectSet</span></span>
```
Stop-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="582bd-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="582bd-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="582bd-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="582bd-108">DESCRIPTION</span></span>
<span data-ttu-id="582bd-109">Os cmdlets **Stop-AzServiceBusMigration** encerram o namespace Migration between Standard to premium</span><span class="sxs-lookup"><span data-stu-id="582bd-109">The **Stop-AzServiceBusMigration** cmdlets terminates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="582bd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="582bd-110">EXAMPLES</span></span>

### <span data-ttu-id="582bd-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="582bd-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="582bd-112">O cmdlet encerra a migração entre o namespace Standard e o namespace Premium fornecido durante a criação da configuração de migração.</span><span class="sxs-lookup"><span data-stu-id="582bd-112">Cmdlet terminates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="582bd-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="582bd-113">PARAMETERS</span></span>

### <span data-ttu-id="582bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="582bd-114">-DefaultProfile</span></span>
<span data-ttu-id="582bd-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="582bd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="582bd-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="582bd-116">-InputObject</span></span>
<span data-ttu-id="582bd-117">Objeto Namespace Padrão de Configuração de Migração de Barramento de Serviço</span><span class="sxs-lookup"><span data-stu-id="582bd-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

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

### <span data-ttu-id="582bd-118">-Name</span><span class="sxs-lookup"><span data-stu-id="582bd-118">-Name</span></span>
<span data-ttu-id="582bd-119">Nome do Namespace Padrão</span><span class="sxs-lookup"><span data-stu-id="582bd-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="582bd-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="582bd-120">-PassThru</span></span>
<span data-ttu-id="582bd-121">Especificar isso retornará true se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="582bd-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="582bd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="582bd-122">-ResourceGroupName</span></span>
<span data-ttu-id="582bd-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="582bd-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="582bd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="582bd-124">-ResourceId</span></span>
<span data-ttu-id="582bd-125">ID do recurso namespace padrão de configuração de migração de barramento de serviço</span><span class="sxs-lookup"><span data-stu-id="582bd-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="582bd-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="582bd-126">-Confirm</span></span>
<span data-ttu-id="582bd-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="582bd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="582bd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="582bd-128">-WhatIf</span></span>
<span data-ttu-id="582bd-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="582bd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="582bd-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="582bd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="582bd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="582bd-131">CommonParameters</span></span>
<span data-ttu-id="582bd-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="582bd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="582bd-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="582bd-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="582bd-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="582bd-134">INPUTS</span></span>

### <span data-ttu-id="582bd-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="582bd-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="582bd-136">System.String</span><span class="sxs-lookup"><span data-stu-id="582bd-136">System.String</span></span>

## <span data-ttu-id="582bd-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="582bd-137">OUTPUTS</span></span>

### <span data-ttu-id="582bd-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="582bd-138">System.Boolean</span></span>

## <span data-ttu-id="582bd-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="582bd-139">NOTES</span></span>

## <span data-ttu-id="582bd-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="582bd-140">RELATED LINKS</span></span>
