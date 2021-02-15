---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/stop-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
ms.openlocfilehash: 615a09d735867d45f9db75ce229d39bc8d9bf75b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111363"
---
# <span data-ttu-id="10c2b-101">Stop-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="10c2b-101">Stop-AzServiceBusMigration</span></span>

## <span data-ttu-id="10c2b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10c2b-102">SYNOPSIS</span></span>
<span data-ttu-id="10c2b-103">{{Fill in the Synopsis}}</span><span class="sxs-lookup"><span data-stu-id="10c2b-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="10c2b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10c2b-104">SYNTAX</span></span>

### <span data-ttu-id="10c2b-105">MigrationConfigurationPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="10c2b-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10c2b-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="10c2b-106">NamespaceInputObjectSet</span></span>
```
Stop-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10c2b-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10c2b-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10c2b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="10c2b-108">DESCRIPTION</span></span>
<span data-ttu-id="10c2b-109">Os cmdlets **Stop-AzServiceBusMigration** encerram a Migração entre o Namespace Padrão para o namespace premium</span><span class="sxs-lookup"><span data-stu-id="10c2b-109">The **Stop-AzServiceBusMigration** cmdlets terminates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="10c2b-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="10c2b-110">EXAMPLES</span></span>

### <span data-ttu-id="10c2b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="10c2b-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="10c2b-112">O Cmdlet encerra a migração entre o namespace padrão e o namespace Premium fornecido durante a criação da configuração de migração.</span><span class="sxs-lookup"><span data-stu-id="10c2b-112">Cmdlet terminates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="10c2b-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10c2b-113">PARAMETERS</span></span>

### <span data-ttu-id="10c2b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10c2b-114">-DefaultProfile</span></span>
<span data-ttu-id="10c2b-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="10c2b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10c2b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10c2b-116">-InputObject</span></span>
<span data-ttu-id="10c2b-117">Objeto Namespace Padrão de Configuração de Migração de Barra de Serviço</span><span class="sxs-lookup"><span data-stu-id="10c2b-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

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

### <span data-ttu-id="10c2b-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="10c2b-118">-Name</span></span>
<span data-ttu-id="10c2b-119">Nome do Namespace Padrão</span><span class="sxs-lookup"><span data-stu-id="10c2b-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="10c2b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10c2b-120">-PassThru</span></span>
<span data-ttu-id="10c2b-121">Especificar isso retornará verdadeiro se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="10c2b-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="10c2b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10c2b-122">-ResourceGroupName</span></span>
<span data-ttu-id="10c2b-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="10c2b-123">Resource Group Name</span></span>

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

### <span data-ttu-id="10c2b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10c2b-124">-ResourceId</span></span>
<span data-ttu-id="10c2b-125">ID do Recurso Namespace Padrão de Configuração de Migração de Barra de Serviço</span><span class="sxs-lookup"><span data-stu-id="10c2b-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="10c2b-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="10c2b-126">-Confirm</span></span>
<span data-ttu-id="10c2b-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10c2b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10c2b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10c2b-128">-WhatIf</span></span>
<span data-ttu-id="10c2b-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="10c2b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10c2b-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="10c2b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10c2b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10c2b-131">CommonParameters</span></span>
<span data-ttu-id="10c2b-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10c2b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10c2b-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10c2b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10c2b-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="10c2b-134">INPUTS</span></span>

### <span data-ttu-id="10c2b-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="10c2b-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="10c2b-136">System.String</span><span class="sxs-lookup"><span data-stu-id="10c2b-136">System.String</span></span>

## <span data-ttu-id="10c2b-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="10c2b-137">OUTPUTS</span></span>

### <span data-ttu-id="10c2b-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="10c2b-138">System.Boolean</span></span>

## <span data-ttu-id="10c2b-139">Notas</span><span class="sxs-lookup"><span data-stu-id="10c2b-139">NOTES</span></span>

## <span data-ttu-id="10c2b-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10c2b-140">RELATED LINKS</span></span>
