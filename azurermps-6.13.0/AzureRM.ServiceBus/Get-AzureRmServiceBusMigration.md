---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusMigration.md
ms.openlocfilehash: cdf869f13c90982c40568f37c0757ef2e7547b3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430867"
---
# <span data-ttu-id="aaedf-101">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="aaedf-101">Get-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="aaedf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aaedf-102">SYNOPSIS</span></span>
<span data-ttu-id="aaedf-103">Recupera MigrationConfiguration para o namespace</span><span class="sxs-lookup"><span data-stu-id="aaedf-103">Retrieves MigrationConfiguration for the namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aaedf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aaedf-104">SYNTAX</span></span>

### <span data-ttu-id="aaedf-105">MigrationConfigurationPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="aaedf-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aaedf-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="aaedf-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmServiceBusMigration [-InputObject] <PSNamespaceAttributes>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aaedf-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aaedf-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aaedf-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aaedf-108">DESCRIPTION</span></span>
<span data-ttu-id="aaedf-109">O **Get-AzureRmServiceBusMigration** recupera a configuração de migração para o namespace</span><span class="sxs-lookup"><span data-stu-id="aaedf-109">The **Get-AzureRmServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="aaedf-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aaedf-110">EXAMPLES</span></span>

### <span data-ttu-id="aaedf-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="aaedf-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Succeeded
PendingReplicationOperationsCount : 40
TargetNamespace   : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="aaedf-112">Obtém as propriedades de configuração de migração de ' TestingNamespaceStandardMirgation '</span><span class="sxs-lookup"><span data-stu-id="aaedf-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMirgation'</span></span>

## <span data-ttu-id="aaedf-113">OS</span><span class="sxs-lookup"><span data-stu-id="aaedf-113">PARAMETERS</span></span>

### <span data-ttu-id="aaedf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaedf-114">-DefaultProfile</span></span>
<span data-ttu-id="aaedf-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aaedf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaedf-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aaedf-116">-InputObject</span></span>
<span data-ttu-id="aaedf-117">Objeto namespace</span><span class="sxs-lookup"><span data-stu-id="aaedf-117">Namespace Object</span></span>

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

### <span data-ttu-id="aaedf-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="aaedf-118">-Name</span></span>
<span data-ttu-id="aaedf-119">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="aaedf-119">Namespace Name</span></span>

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

### <span data-ttu-id="aaedf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaedf-120">-ResourceGroupName</span></span>
<span data-ttu-id="aaedf-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="aaedf-121">Resource Group Name</span></span>

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

### <span data-ttu-id="aaedf-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aaedf-122">-ResourceId</span></span>
<span data-ttu-id="aaedf-123">ID do recurso namespace</span><span class="sxs-lookup"><span data-stu-id="aaedf-123">Namespace Resource Id</span></span>

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

### <span data-ttu-id="aaedf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaedf-124">CommonParameters</span></span>
<span data-ttu-id="aaedf-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaedf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaedf-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaedf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaedf-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aaedf-127">INPUTS</span></span>

### <span data-ttu-id="aaedf-128">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="aaedf-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="aaedf-129">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="aaedf-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="aaedf-130">System. String</span><span class="sxs-lookup"><span data-stu-id="aaedf-130">System.String</span></span>

## <span data-ttu-id="aaedf-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aaedf-131">OUTPUTS</span></span>

### <span data-ttu-id="aaedf-132">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="aaedf-132">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="aaedf-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aaedf-133">NOTES</span></span>

## <span data-ttu-id="aaedf-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aaedf-134">RELATED LINKS</span></span>
