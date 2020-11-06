---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusMigration.md
ms.openlocfilehash: c378f6315f66b7149c1a8bb6d51ce806425065a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429335"
---
# <span data-ttu-id="f572a-101">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="f572a-101">Remove-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="f572a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f572a-102">SYNOPSIS</span></span>
<span data-ttu-id="f572a-103">Cmdlet exclui a configuração de migração de namespaces padrão para Premium</span><span class="sxs-lookup"><span data-stu-id="f572a-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f572a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f572a-104">SYNTAX</span></span>

### <span data-ttu-id="f572a-105">MigrationConfigurationPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f572a-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f572a-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f572a-106">NamespaceInputObjectSet</span></span>
```
Remove-AzureRmServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f572a-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f572a-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f572a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f572a-108">DESCRIPTION</span></span>
<span data-ttu-id="f572a-109">O cmdlet **Remove-AzureRmServiceBusMigration** exclui a configuração de migração para namespaces padrão para Premium</span><span class="sxs-lookup"><span data-stu-id="f572a-109">The **Remove-AzureRmServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="f572a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f572a-110">EXAMPLES</span></span>

### <span data-ttu-id="f572a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f572a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation
```

<span data-ttu-id="f572a-112">Exclui a configuração de migração ' TestingNamespaceStandardMirgation '</span><span class="sxs-lookup"><span data-stu-id="f572a-112">Deletes the 'TestingNamespaceStandardMirgation' migration configuration</span></span>

## <span data-ttu-id="f572a-113">OS</span><span class="sxs-lookup"><span data-stu-id="f572a-113">PARAMETERS</span></span>

### <span data-ttu-id="f572a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f572a-114">-AsJob</span></span>
<span data-ttu-id="f572a-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f572a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f572a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f572a-116">-DefaultProfile</span></span>
<span data-ttu-id="f572a-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f572a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f572a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f572a-118">-InputObject</span></span>
<span data-ttu-id="f572a-119">Objeto namespace padrão de migração do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="f572a-119">Service Bus Migration Standard Namespace Object</span></span>

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

### <span data-ttu-id="f572a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f572a-120">-Name</span></span>
<span data-ttu-id="f572a-121">Nome do namespace padrão</span><span class="sxs-lookup"><span data-stu-id="f572a-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="f572a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f572a-122">-PassThru</span></span>
<span data-ttu-id="f572a-123">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f572a-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="f572a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f572a-124">-ResourceGroupName</span></span>
<span data-ttu-id="f572a-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f572a-125">Resource Group Name</span></span>

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

### <span data-ttu-id="f572a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f572a-126">-ResourceId</span></span>
<span data-ttu-id="f572a-127">ID do recurso namespace padrão da migração do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="f572a-127">Service Bus Migration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="f572a-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f572a-128">-Confirm</span></span>
<span data-ttu-id="f572a-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f572a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f572a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f572a-130">-WhatIf</span></span>
<span data-ttu-id="f572a-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f572a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f572a-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f572a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f572a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f572a-133">CommonParameters</span></span>
<span data-ttu-id="f572a-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f572a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f572a-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f572a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f572a-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f572a-136">INPUTS</span></span>

### <span data-ttu-id="f572a-137">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="f572a-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="f572a-138">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f572a-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="f572a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f572a-139">System.String</span></span>

## <span data-ttu-id="f572a-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f572a-140">OUTPUTS</span></span>

### <span data-ttu-id="f572a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f572a-141">System.Boolean</span></span>

## <span data-ttu-id="f572a-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f572a-142">NOTES</span></span>

## <span data-ttu-id="f572a-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f572a-143">RELATED LINKS</span></span>