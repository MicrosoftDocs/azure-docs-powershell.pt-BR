---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 59b4ad9eb439808033233aa1677be16862c8a973
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433564"
---
# <span data-ttu-id="30e46-101">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="30e46-101">Get-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="30e46-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="30e46-102">SYNOPSIS</span></span>
<span data-ttu-id="30e46-103">Obtém um assembly da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="30e46-103">Gets an integration account assembly.</span></span>

## <span data-ttu-id="30e46-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="30e46-104">SYNTAX</span></span>

### <span data-ttu-id="30e46-105">ByIntegrationAccount (padrão)</span><span class="sxs-lookup"><span data-stu-id="30e46-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30e46-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="30e46-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30e46-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="30e46-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountAssembly -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30e46-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="30e46-108">DESCRIPTION</span></span>
<span data-ttu-id="30e46-109">O cmdlet **Get-AzIntegrationAccountAssembly** Obtém um assembly de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="30e46-109">The **Get-AzIntegrationAccountAssembly** cmdlet gets an assembly from an integration account.</span></span>

## <span data-ttu-id="30e46-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="30e46-110">EXAMPLES</span></span>

### <span data-ttu-id="30e46-111">Exemplo 1: obter um assembly por parâmetros</span><span class="sxs-lookup"><span data-stu-id="30e46-111">Example 1: Get an assembly by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="30e46-112">Obtenha um assembly chamado "sampleAssembly" localizado na conta de integração "sampleIntegrationAccount" que está contido no grupo de recursos "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="30e46-112">Get an assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="30e46-113">Exemplo 2: listar todos os assemblies em uma conta de integração por parâmetros</span><span class="sxs-lookup"><span data-stu-id="30e46-113">Example 2: List all assemblies in an integration account by parameters</span></span>
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

<span data-ttu-id="30e46-114">Obtenha todos os assemblies localizados na conta de integração "sampleIntegrationAccount" que está contida no grupo de recursos "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="30e46-114">Get all assemblies located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="30e46-115">OS</span><span class="sxs-lookup"><span data-stu-id="30e46-115">PARAMETERS</span></span>

### <span data-ttu-id="30e46-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30e46-116">-DefaultProfile</span></span>
<span data-ttu-id="30e46-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="30e46-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30e46-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="30e46-118">-Name</span></span>
<span data-ttu-id="30e46-119">O nome do assembly da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="30e46-119">The integration account assembly name.</span></span>

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

### <span data-ttu-id="30e46-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="30e46-120">-ParentName</span></span>
<span data-ttu-id="30e46-121">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="30e46-121">The integration account name.</span></span>

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

### <span data-ttu-id="30e46-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="30e46-122">-ParentObject</span></span>
<span data-ttu-id="30e46-123">Um objeto de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="30e46-123">An integration account object.</span></span>

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

### <span data-ttu-id="30e46-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="30e46-124">-ParentResourceId</span></span>
<span data-ttu-id="30e46-125">A ID do recurso da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="30e46-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="30e46-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30e46-126">-ResourceGroupName</span></span>
<span data-ttu-id="30e46-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="30e46-127">The resource group name.</span></span>

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

### <span data-ttu-id="30e46-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30e46-128">CommonParameters</span></span>
<span data-ttu-id="30e46-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30e46-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30e46-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30e46-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30e46-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="30e46-131">INPUTS</span></span>

### <span data-ttu-id="30e46-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="30e46-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="30e46-133">System. String</span><span class="sxs-lookup"><span data-stu-id="30e46-133">System.String</span></span>

## <span data-ttu-id="30e46-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="30e46-134">OUTPUTS</span></span>

### <span data-ttu-id="30e46-135">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="30e46-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="30e46-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="30e46-136">NOTES</span></span>

## <span data-ttu-id="30e46-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="30e46-137">RELATED LINKS</span></span>
