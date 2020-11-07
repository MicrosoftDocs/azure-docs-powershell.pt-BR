---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
ms.openlocfilehash: 1e782c381ec10d03f269fc0a2d0871f064e4ddef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772481"
---
# <span data-ttu-id="75e2f-101">Get-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="75e2f-101">Get-AzServiceBusMigration</span></span>

## <span data-ttu-id="75e2f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75e2f-102">SYNOPSIS</span></span>
<span data-ttu-id="75e2f-103">Recupera MigrationConfiguration para o namespace</span><span class="sxs-lookup"><span data-stu-id="75e2f-103">Retrieves MigrationConfiguration for the namespace</span></span>

## <span data-ttu-id="75e2f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75e2f-104">SYNTAX</span></span>

### <span data-ttu-id="75e2f-105">MigrationConfigurationPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="75e2f-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75e2f-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="75e2f-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusMigration [-InputObject] <PSNamespaceAttributes> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="75e2f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75e2f-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75e2f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75e2f-108">DESCRIPTION</span></span>
<span data-ttu-id="75e2f-109">O **Get-AzServiceBusMigration** recupera a configuração de migração para o namespace</span><span class="sxs-lookup"><span data-stu-id="75e2f-109">The **Get-AzServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="75e2f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75e2f-110">EXAMPLES</span></span>

### <span data-ttu-id="75e2f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="75e2f-111">Example 1</span></span>
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

<span data-ttu-id="75e2f-112">Obtém as propriedades de configuração de migração de ' TestingNamespaceStandardMigration '</span><span class="sxs-lookup"><span data-stu-id="75e2f-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMigration'</span></span>

## <span data-ttu-id="75e2f-113">OS</span><span class="sxs-lookup"><span data-stu-id="75e2f-113">PARAMETERS</span></span>

### <span data-ttu-id="75e2f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75e2f-114">-DefaultProfile</span></span>
<span data-ttu-id="75e2f-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75e2f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75e2f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75e2f-116">-InputObject</span></span>
<span data-ttu-id="75e2f-117">Objeto namespace</span><span class="sxs-lookup"><span data-stu-id="75e2f-117">Namespace Object</span></span>

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

### <span data-ttu-id="75e2f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="75e2f-118">-Name</span></span>
<span data-ttu-id="75e2f-119">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="75e2f-119">Namespace Name</span></span>

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

### <span data-ttu-id="75e2f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75e2f-120">-ResourceGroupName</span></span>
<span data-ttu-id="75e2f-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="75e2f-121">Resource Group Name</span></span>

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

### <span data-ttu-id="75e2f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75e2f-122">-ResourceId</span></span>
<span data-ttu-id="75e2f-123">ID do recurso namespace</span><span class="sxs-lookup"><span data-stu-id="75e2f-123">Namespace Resource Id</span></span>

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

### <span data-ttu-id="75e2f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75e2f-124">CommonParameters</span></span>
<span data-ttu-id="75e2f-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75e2f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75e2f-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75e2f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75e2f-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75e2f-127">INPUTS</span></span>

### <span data-ttu-id="75e2f-128">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="75e2f-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="75e2f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="75e2f-129">System.String</span></span>

## <span data-ttu-id="75e2f-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75e2f-130">OUTPUTS</span></span>

### <span data-ttu-id="75e2f-131">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="75e2f-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="75e2f-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75e2f-132">NOTES</span></span>

## <span data-ttu-id="75e2f-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75e2f-133">RELATED LINKS</span></span>
