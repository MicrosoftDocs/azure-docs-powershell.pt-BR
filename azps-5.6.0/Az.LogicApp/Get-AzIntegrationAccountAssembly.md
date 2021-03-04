---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 95daa8025dde470e85d0e00e09c00f26d08e1342
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892627"
---
# <span data-ttu-id="d8dbc-101">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d8dbc-101">Get-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="d8dbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8dbc-102">SYNOPSIS</span></span>
<span data-ttu-id="d8dbc-103">Obtém um assembly de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-103">Gets an integration account assembly.</span></span>

## <span data-ttu-id="d8dbc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d8dbc-104">SYNTAX</span></span>

### <span data-ttu-id="d8dbc-105">ByIntegrationAccount (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d8dbc-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8dbc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d8dbc-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8dbc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d8dbc-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountAssembly -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8dbc-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d8dbc-108">DESCRIPTION</span></span>
<span data-ttu-id="d8dbc-109">O cmdlet **Get-AzIntegrationAccountAssembly** obtém um assembly de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-109">The **Get-AzIntegrationAccountAssembly** cmdlet gets an assembly from an integration account.</span></span>

## <span data-ttu-id="d8dbc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8dbc-110">EXAMPLES</span></span>

### <span data-ttu-id="d8dbc-111">Exemplo 1: Obter um assembly por parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8dbc-111">Example 1: Get an assembly by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="d8dbc-112">Obter um assembly chamado "sampleAssembly" localizado na conta de integração "sampleIntegrationAccount" que está contida no grupo de recursos "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="d8dbc-112">Get an assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="d8dbc-113">Exemplo 2: Listar todos os assemblies em uma conta de integração por parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8dbc-113">Example 2: List all assemblies in an integration account by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly2
Name       : sampleAssembly2
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="d8dbc-114">Obter todos os assemblies localizados na conta de integração "sampleIntegrationAccount" que está contida no grupo de recursos "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="d8dbc-114">Get all assemblies located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="d8dbc-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d8dbc-115">PARAMETERS</span></span>

### <span data-ttu-id="d8dbc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8dbc-116">-DefaultProfile</span></span>
<span data-ttu-id="d8dbc-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8dbc-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d8dbc-118">-Name</span></span>
<span data-ttu-id="d8dbc-119">O nome do assembly da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-119">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssemblyName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dbc-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="d8dbc-120">-ParentName</span></span>
<span data-ttu-id="d8dbc-121">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dbc-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d8dbc-122">-ParentObject</span></span>
<span data-ttu-id="d8dbc-123">Um objeto de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-123">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8dbc-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d8dbc-124">-ParentResourceId</span></span>
<span data-ttu-id="d8dbc-125">A ID do recurso de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-125">The integration account resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8dbc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8dbc-126">-ResourceGroupName</span></span>
<span data-ttu-id="d8dbc-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dbc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8dbc-128">CommonParameters</span></span>
<span data-ttu-id="d8dbc-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8dbc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8dbc-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8dbc-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8dbc-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8dbc-131">INPUTS</span></span>

### <span data-ttu-id="d8dbc-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d8dbc-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="d8dbc-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d8dbc-133">System.String</span></span>

## <span data-ttu-id="d8dbc-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d8dbc-134">OUTPUTS</span></span>

### <span data-ttu-id="d8dbc-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d8dbc-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="d8dbc-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="d8dbc-136">NOTES</span></span>

## <span data-ttu-id="d8dbc-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8dbc-137">RELATED LINKS</span></span>
