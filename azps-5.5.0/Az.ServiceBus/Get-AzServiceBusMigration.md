---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
ms.openlocfilehash: 686a2486d6a5e28e0149eb8fbf2387744d545fd0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116184"
---
# <span data-ttu-id="b1c27-101">Get-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b1c27-101">Get-AzServiceBusMigration</span></span>

## <span data-ttu-id="b1c27-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b1c27-102">SYNOPSIS</span></span>
<span data-ttu-id="b1c27-103">Recupera MigrationConfiguration para o namespace</span><span class="sxs-lookup"><span data-stu-id="b1c27-103">Retrieves MigrationConfiguration for the namespace</span></span>

## <span data-ttu-id="b1c27-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1c27-104">SYNTAX</span></span>

### <span data-ttu-id="b1c27-105">MigrationConfigurationPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b1c27-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1c27-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b1c27-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusMigration [-InputObject] <PSNamespaceAttributes> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b1c27-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1c27-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1c27-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1c27-108">DESCRIPTION</span></span>
<span data-ttu-id="b1c27-109">A Configuração de Migração **do Get-AzServiceBusMigration** recupera a configuração de migração para o namespace</span><span class="sxs-lookup"><span data-stu-id="b1c27-109">The **Get-AzServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="b1c27-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b1c27-110">EXAMPLES</span></span>

### <span data-ttu-id="b1c27-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b1c27-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Succeeded
PendingReplicationOperationsCount : 40
TargetNamespace   : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="b1c27-112">Obtém as propriedades de Configuração de Migração de 'TestingNamespaceStandardMigration'</span><span class="sxs-lookup"><span data-stu-id="b1c27-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMigration'</span></span>

## <span data-ttu-id="b1c27-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1c27-113">PARAMETERS</span></span>

### <span data-ttu-id="b1c27-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1c27-114">-DefaultProfile</span></span>
<span data-ttu-id="b1c27-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b1c27-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1c27-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1c27-116">-InputObject</span></span>
<span data-ttu-id="b1c27-117">Objeto Namespace</span><span class="sxs-lookup"><span data-stu-id="b1c27-117">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1c27-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1c27-118">-Name</span></span>
<span data-ttu-id="b1c27-119">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="b1c27-119">Namespace Name</span></span>

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

### <span data-ttu-id="b1c27-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1c27-120">-ResourceGroupName</span></span>
<span data-ttu-id="b1c27-121">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="b1c27-121">Resource Group Name</span></span>

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

### <span data-ttu-id="b1c27-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1c27-122">-ResourceId</span></span>
<span data-ttu-id="b1c27-123">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="b1c27-123">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1c27-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1c27-124">CommonParameters</span></span>
<span data-ttu-id="b1c27-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1c27-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1c27-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1c27-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1c27-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="b1c27-127">INPUTS</span></span>

### <span data-ttu-id="b1c27-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="b1c27-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="b1c27-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b1c27-129">System.String</span></span>

## <span data-ttu-id="b1c27-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="b1c27-130">OUTPUTS</span></span>

### <span data-ttu-id="b1c27-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="b1c27-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="b1c27-132">Notas</span><span class="sxs-lookup"><span data-stu-id="b1c27-132">NOTES</span></span>

## <span data-ttu-id="b1c27-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1c27-133">RELATED LINKS</span></span>
