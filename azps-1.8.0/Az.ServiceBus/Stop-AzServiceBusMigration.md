---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/stop-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
ms.openlocfilehash: c507caa0ce6697132876309a7ae816802a682683
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599132"
---
# <span data-ttu-id="1be03-101">Stop-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="1be03-101">Stop-AzServiceBusMigration</span></span>

## <span data-ttu-id="1be03-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1be03-102">SYNOPSIS</span></span>
<span data-ttu-id="1be03-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="1be03-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="1be03-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1be03-104">SYNTAX</span></span>

### <span data-ttu-id="1be03-105">MigrationConfigurationPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1be03-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1be03-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1be03-106">NamespaceInputObjectSet</span></span>
```
Stop-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1be03-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1be03-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1be03-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1be03-108">DESCRIPTION</span></span>
<span data-ttu-id="1be03-109">Os cmdlets **Stop-AzServiceBusMigration** terminam a migração entre o namespace padrão Premium</span><span class="sxs-lookup"><span data-stu-id="1be03-109">The **Stop-AzServiceBusMigration** cmdlets terminates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="1be03-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1be03-110">EXAMPLES</span></span>

### <span data-ttu-id="1be03-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1be03-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation
```

<span data-ttu-id="1be03-112">O cmdlet termina a migração entre namespace padrão e namespace Premium fornecido durante a criação da configuração de migração.</span><span class="sxs-lookup"><span data-stu-id="1be03-112">Cmdlet terminates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="1be03-113">OS</span><span class="sxs-lookup"><span data-stu-id="1be03-113">PARAMETERS</span></span>

### <span data-ttu-id="1be03-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1be03-114">-DefaultProfile</span></span>
<span data-ttu-id="1be03-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1be03-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1be03-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1be03-116">-InputObject</span></span>
<span data-ttu-id="1be03-117">Objeto namespace padrão de configuração de migração do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="1be03-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

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

### <span data-ttu-id="1be03-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="1be03-118">-Name</span></span>
<span data-ttu-id="1be03-119">Nome do namespace padrão</span><span class="sxs-lookup"><span data-stu-id="1be03-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="1be03-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1be03-120">-PassThru</span></span>
<span data-ttu-id="1be03-121">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="1be03-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="1be03-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1be03-122">-ResourceGroupName</span></span>
<span data-ttu-id="1be03-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1be03-123">Resource Group Name</span></span>

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

### <span data-ttu-id="1be03-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1be03-124">-ResourceId</span></span>
<span data-ttu-id="1be03-125">ID do recurso namespace padrão de configuração de migração do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="1be03-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="1be03-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1be03-126">-Confirm</span></span>
<span data-ttu-id="1be03-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1be03-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1be03-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1be03-128">-WhatIf</span></span>
<span data-ttu-id="1be03-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1be03-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1be03-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1be03-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1be03-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1be03-131">CommonParameters</span></span>
<span data-ttu-id="1be03-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1be03-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1be03-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1be03-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1be03-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1be03-134">INPUTS</span></span>

### <span data-ttu-id="1be03-135">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="1be03-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="1be03-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1be03-136">System.String</span></span>

## <span data-ttu-id="1be03-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1be03-137">OUTPUTS</span></span>

### <span data-ttu-id="1be03-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1be03-138">System.Boolean</span></span>

## <span data-ttu-id="1be03-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1be03-139">NOTES</span></span>

## <span data-ttu-id="1be03-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1be03-140">RELATED LINKS</span></span>
