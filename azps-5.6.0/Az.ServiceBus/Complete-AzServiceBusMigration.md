---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/complete-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
ms.openlocfilehash: 3d993e95eb3a92e5b0894e020af06d2d88b8ed4d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893107"
---
# <span data-ttu-id="afbed-101">Complete-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="afbed-101">Complete-AzServiceBusMigration</span></span>

## <span data-ttu-id="afbed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afbed-102">SYNOPSIS</span></span>
<span data-ttu-id="afbed-103">Os cmdlets definiram a Migração do namespace Standard para o premium como cadeias de caracteres completas e de conexão do namespace padrão agora apontam para o namespace Premium</span><span class="sxs-lookup"><span data-stu-id="afbed-103">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="afbed-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="afbed-104">SYNTAX</span></span>

### <span data-ttu-id="afbed-105">MigrationConfigurationPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="afbed-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Complete-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afbed-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="afbed-106">NamespaceInputObjectSet</span></span>
```
Complete-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afbed-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="afbed-107">NamespaceResourceIdParameterSet</span></span>
```
Complete-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afbed-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="afbed-108">DESCRIPTION</span></span>
<span data-ttu-id="afbed-109">Os cmdlets **Complete-AzServiceBusMigration** definirão o namespace Migration from Standard para premium como cadeias de caracteres completas e de conexão do namespace padrão agora apontam para namespace Premium</span><span class="sxs-lookup"><span data-stu-id="afbed-109">The **Complete-AzServiceBusMigration** cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="afbed-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="afbed-110">EXAMPLES</span></span>

### <span data-ttu-id="afbed-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="afbed-111">Example 1</span></span>
```powershell
PS C:\> Complete-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name NamespaceStandardMigration
```

<span data-ttu-id="afbed-112">Define a migração do namespace 'NamespaceStandardMigration' como concluída.</span><span class="sxs-lookup"><span data-stu-id="afbed-112">Sets the Migration of 'NamespaceStandardMigration' namespace as complete.</span></span>

## <span data-ttu-id="afbed-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="afbed-113">PARAMETERS</span></span>

### <span data-ttu-id="afbed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afbed-114">-DefaultProfile</span></span>
<span data-ttu-id="afbed-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="afbed-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afbed-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afbed-116">-InputObject</span></span>
<span data-ttu-id="afbed-117">Configuração de Migração de Barramento de Serviço - Objeto Namespace Padrão</span><span class="sxs-lookup"><span data-stu-id="afbed-117">Service Bus Migration configuration - Standard Namespace Object</span></span>

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

### <span data-ttu-id="afbed-118">-Name</span><span class="sxs-lookup"><span data-stu-id="afbed-118">-Name</span></span>
<span data-ttu-id="afbed-119">Nome do Namespace Padrão</span><span class="sxs-lookup"><span data-stu-id="afbed-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="afbed-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="afbed-120">-PassThru</span></span>
<span data-ttu-id="afbed-121">Especificar isso retornará true se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="afbed-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="afbed-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afbed-122">-ResourceGroupName</span></span>
<span data-ttu-id="afbed-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="afbed-123">Resource Group Name</span></span>

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

### <span data-ttu-id="afbed-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afbed-124">-ResourceId</span></span>
<span data-ttu-id="afbed-125">Migração de Barramento de Serviço - ID de Recurso de Namespace Padrão</span><span class="sxs-lookup"><span data-stu-id="afbed-125">Service Bus Migration - Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="afbed-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afbed-126">-Confirm</span></span>
<span data-ttu-id="afbed-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afbed-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afbed-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afbed-128">-WhatIf</span></span>
<span data-ttu-id="afbed-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="afbed-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afbed-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="afbed-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afbed-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afbed-131">CommonParameters</span></span>
<span data-ttu-id="afbed-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afbed-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afbed-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afbed-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afbed-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="afbed-134">INPUTS</span></span>

### <span data-ttu-id="afbed-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="afbed-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="afbed-136">System.String</span><span class="sxs-lookup"><span data-stu-id="afbed-136">System.String</span></span>

## <span data-ttu-id="afbed-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="afbed-137">OUTPUTS</span></span>

### <span data-ttu-id="afbed-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="afbed-138">System.Boolean</span></span>

## <span data-ttu-id="afbed-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="afbed-139">NOTES</span></span>

## <span data-ttu-id="afbed-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="afbed-140">RELATED LINKS</span></span>
