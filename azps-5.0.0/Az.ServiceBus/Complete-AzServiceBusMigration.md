---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/complete-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
ms.openlocfilehash: 883ecf9337cea2b46166b4c1be8625c9763eb7db
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125085"
---
# <span data-ttu-id="f620d-101">Complete-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="f620d-101">Complete-AzServiceBusMigration</span></span>

## <span data-ttu-id="f620d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f620d-102">SYNOPSIS</span></span>
<span data-ttu-id="f620d-103">Cmdlets definem a migração do namespace Standard para Premium como cadeias de caracteres de conexão completa e de conexão do namespace padrão apontam para namespace Premium</span><span class="sxs-lookup"><span data-stu-id="f620d-103">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="f620d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f620d-104">SYNTAX</span></span>

### <span data-ttu-id="f620d-105">MigrationConfigurationPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f620d-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Complete-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f620d-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f620d-106">NamespaceInputObjectSet</span></span>
```
Complete-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f620d-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f620d-107">NamespaceResourceIdParameterSet</span></span>
```
Complete-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f620d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f620d-108">DESCRIPTION</span></span>
<span data-ttu-id="f620d-109">Os cmdlets **Complete-AzServiceBusMigration** definem a migração do namespace padrão para Premium, já que cadeias de caracteres de conexão completa e de conexão do namespace padrão apontam para namespace Premium</span><span class="sxs-lookup"><span data-stu-id="f620d-109">The **Complete-AzServiceBusMigration** cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="f620d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f620d-110">EXAMPLES</span></span>

### <span data-ttu-id="f620d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f620d-111">Example 1</span></span>
```powershell
PS C:\> Complete-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name NamespaceStandardMigration
```

<span data-ttu-id="f620d-112">Define a migração do namespace ' NamespaceStandardMigration ' como concluída.</span><span class="sxs-lookup"><span data-stu-id="f620d-112">Sets the Migration of 'NamespaceStandardMigration' namespace as complete.</span></span>

## <span data-ttu-id="f620d-113">OS</span><span class="sxs-lookup"><span data-stu-id="f620d-113">PARAMETERS</span></span>

### <span data-ttu-id="f620d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f620d-114">-DefaultProfile</span></span>
<span data-ttu-id="f620d-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f620d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f620d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f620d-116">-InputObject</span></span>
<span data-ttu-id="f620d-117">Configuração de migração de barramento de serviço-objeto de namespace padrão</span><span class="sxs-lookup"><span data-stu-id="f620d-117">Service Bus Migration configuration - Standard Namespace Object</span></span>

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

### <span data-ttu-id="f620d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="f620d-118">-Name</span></span>
<span data-ttu-id="f620d-119">Nome do namespace padrão</span><span class="sxs-lookup"><span data-stu-id="f620d-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="f620d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f620d-120">-PassThru</span></span>
<span data-ttu-id="f620d-121">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f620d-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="f620d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f620d-122">-ResourceGroupName</span></span>
<span data-ttu-id="f620d-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f620d-123">Resource Group Name</span></span>

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

### <span data-ttu-id="f620d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f620d-124">-ResourceId</span></span>
<span data-ttu-id="f620d-125">Migração do barramento do serviço-ID do recurso namespace padrão</span><span class="sxs-lookup"><span data-stu-id="f620d-125">Service Bus Migration - Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="f620d-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f620d-126">-Confirm</span></span>
<span data-ttu-id="f620d-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f620d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f620d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f620d-128">-WhatIf</span></span>
<span data-ttu-id="f620d-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f620d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f620d-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f620d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f620d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f620d-131">CommonParameters</span></span>
<span data-ttu-id="f620d-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f620d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f620d-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f620d-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f620d-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f620d-134">INPUTS</span></span>

### <span data-ttu-id="f620d-135">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="f620d-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="f620d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f620d-136">System.String</span></span>

## <span data-ttu-id="f620d-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f620d-137">OUTPUTS</span></span>

### <span data-ttu-id="f620d-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f620d-138">System.Boolean</span></span>

## <span data-ttu-id="f620d-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f620d-139">NOTES</span></span>

## <span data-ttu-id="f620d-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f620d-140">RELATED LINKS</span></span>
