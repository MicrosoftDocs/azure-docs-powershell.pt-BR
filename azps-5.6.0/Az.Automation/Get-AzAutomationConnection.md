---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
ms.openlocfilehash: 5332cb1ca52a8ee3e7685ecf2fd36fd2333fd453
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891235"
---
# <span data-ttu-id="9a0cc-101">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9a0cc-101">Get-AzAutomationConnection</span></span>

## <span data-ttu-id="9a0cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a0cc-102">SYNOPSIS</span></span>
<span data-ttu-id="9a0cc-103">Obtém uma conexão de automação.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-103">Gets an Automation connection.</span></span>

## <span data-ttu-id="9a0cc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9a0cc-104">SYNTAX</span></span>

### <span data-ttu-id="9a0cc-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9a0cc-105">ByAll (Default)</span></span>
```
Get-AzAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a0cc-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="9a0cc-106">ByConnectionName</span></span>
```
Get-AzAutomationConnection [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a0cc-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="9a0cc-107">ByConnectionTypeName</span></span>
```
Get-AzAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a0cc-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9a0cc-108">DESCRIPTION</span></span>
<span data-ttu-id="9a0cc-109">O cmdlet **Get-AzAutomationConnection** obtém uma ou mais conexões de Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-109">The **Get-AzAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="9a0cc-110">Por padrão, esse cmdlet recupera todas as conexões.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="9a0cc-111">Especifique o nome de uma conexão para obter uma conexão específica.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="9a0cc-112">Especifique o nome do tipo de conexão para obter todas as conexões de um tipo específico.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="9a0cc-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9a0cc-113">EXAMPLES</span></span>

### <span data-ttu-id="9a0cc-114">Exemplo 1: Obter todas as conexões</span><span class="sxs-lookup"><span data-stu-id="9a0cc-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="9a0cc-115">Este comando obtém metadados para todas as conexões na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="9a0cc-116">Exemplo 2: Obter todas as conexões de um tipo</span><span class="sxs-lookup"><span data-stu-id="9a0cc-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="9a0cc-117">Este comando obtém metadados para conexões na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="9a0cc-118">Este comando obtém conexões do tipo SqlServer.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="9a0cc-119">Exemplo 3: Obter uma conexão</span><span class="sxs-lookup"><span data-stu-id="9a0cc-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="9a0cc-120">Este comando obtém metadados para a conexão chamada ContosoConnection.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="9a0cc-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9a0cc-121">PARAMETERS</span></span>

### <span data-ttu-id="9a0cc-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9a0cc-122">-AutomationAccountName</span></span>
<span data-ttu-id="9a0cc-123">Especifica o nome da conta de automação para a qual este cmdlet obtém conexões.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a0cc-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="9a0cc-124">-ConnectionTypeName</span></span>
<span data-ttu-id="9a0cc-125">Especifica o nome de um tipo de conexão para o qual este cmdlet recupera conexões.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConnectionTypeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a0cc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a0cc-126">-DefaultProfile</span></span>
<span data-ttu-id="9a0cc-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="9a0cc-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a0cc-128">-Name</span><span class="sxs-lookup"><span data-stu-id="9a0cc-128">-Name</span></span>
<span data-ttu-id="9a0cc-129">Especifica o nome de uma conexão recuperada por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConnectionName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a0cc-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a0cc-130">-ResourceGroupName</span></span>
<span data-ttu-id="9a0cc-131">Especifica o nome de um grupo de recursos para o qual este cmdlet obtém conexões.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a0cc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a0cc-132">CommonParameters</span></span>
<span data-ttu-id="9a0cc-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a0cc-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a0cc-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a0cc-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a0cc-135">INPUTS</span></span>

### <span data-ttu-id="9a0cc-136">System.String</span><span class="sxs-lookup"><span data-stu-id="9a0cc-136">System.String</span></span>

## <span data-ttu-id="9a0cc-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9a0cc-137">OUTPUTS</span></span>

### <span data-ttu-id="9a0cc-138">Microsoft.Azure.Commands.Automation.Model.Connection</span><span class="sxs-lookup"><span data-stu-id="9a0cc-138">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="9a0cc-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="9a0cc-139">NOTES</span></span>

## <span data-ttu-id="9a0cc-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a0cc-140">RELATED LINKS</span></span>

[<span data-ttu-id="9a0cc-141">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9a0cc-141">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)

[<span data-ttu-id="9a0cc-142">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9a0cc-142">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


