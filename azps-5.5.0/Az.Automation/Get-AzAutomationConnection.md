---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
ms.openlocfilehash: 3cf369be5c7d62d9e4b85002906d55f34a47e40c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117023"
---
# <span data-ttu-id="4d7ef-101">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="4d7ef-101">Get-AzAutomationConnection</span></span>

## <span data-ttu-id="4d7ef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4d7ef-102">SYNOPSIS</span></span>
<span data-ttu-id="4d7ef-103">Obtém uma conexão automação.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-103">Gets an Automation connection.</span></span>

## <span data-ttu-id="4d7ef-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d7ef-104">SYNTAX</span></span>

### <span data-ttu-id="4d7ef-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4d7ef-105">ByAll (Default)</span></span>
```
Get-AzAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d7ef-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="4d7ef-106">ByConnectionName</span></span>
```
Get-AzAutomationConnection [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d7ef-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="4d7ef-107">ByConnectionTypeName</span></span>
```
Get-AzAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d7ef-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4d7ef-108">DESCRIPTION</span></span>
<span data-ttu-id="4d7ef-109">O **cmdlet Get-AzAutomationConnection** obtém uma ou mais conexões de Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-109">The **Get-AzAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="4d7ef-110">Por padrão, esse cmdlet recupera todas as conexões.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="4d7ef-111">Especifique o nome de uma conexão para obter uma conexão específica.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="4d7ef-112">Especifique o nome do tipo de conexão para obter todas as conexões de um tipo específico.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="4d7ef-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4d7ef-113">EXAMPLES</span></span>

### <span data-ttu-id="4d7ef-114">Exemplo 1: Obter todas as conexões</span><span class="sxs-lookup"><span data-stu-id="4d7ef-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="4d7ef-115">Esse comando obtém metadados para todas as conexões na conta automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="4d7ef-116">Exemplo 2: Obter todas as conexões de um tipo</span><span class="sxs-lookup"><span data-stu-id="4d7ef-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="4d7ef-117">Esse comando obtém metadados para conexões na conta automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="4d7ef-118">Esse comando obtém conexões do tipo SqlServer.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="4d7ef-119">Exemplo 3: Obter uma conexão</span><span class="sxs-lookup"><span data-stu-id="4d7ef-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="4d7ef-120">Esse comando obtém metadados para a conexão chamada ContosoConnection.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="4d7ef-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d7ef-121">PARAMETERS</span></span>

### <span data-ttu-id="4d7ef-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4d7ef-122">-AutomationAccountName</span></span>
<span data-ttu-id="4d7ef-123">Especifica o nome da conta automação para a qual este cmdlet obtém conexões.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="4d7ef-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="4d7ef-124">-ConnectionTypeName</span></span>
<span data-ttu-id="4d7ef-125">Especifica o nome de um tipo de conexão para o qual este cmdlet recupera conexões.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

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

### <span data-ttu-id="4d7ef-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d7ef-126">-DefaultProfile</span></span>
<span data-ttu-id="4d7ef-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4d7ef-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d7ef-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d7ef-128">-Name</span></span>
<span data-ttu-id="4d7ef-129">Especifica o nome de uma conexão recuperada por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

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

### <span data-ttu-id="4d7ef-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d7ef-130">-ResourceGroupName</span></span>
<span data-ttu-id="4d7ef-131">Especifica o nome de um grupo de recursos para o qual este cmdlet obtém conexões.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="4d7ef-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d7ef-132">CommonParameters</span></span>
<span data-ttu-id="4d7ef-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d7ef-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d7ef-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d7ef-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="4d7ef-135">INPUTS</span></span>

### <span data-ttu-id="4d7ef-136">System.String</span><span class="sxs-lookup"><span data-stu-id="4d7ef-136">System.String</span></span>

## <span data-ttu-id="4d7ef-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="4d7ef-137">OUTPUTS</span></span>

### <span data-ttu-id="4d7ef-138">Microsoft.Azure.Commands.Automation.Model.Connection</span><span class="sxs-lookup"><span data-stu-id="4d7ef-138">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="4d7ef-139">Notas</span><span class="sxs-lookup"><span data-stu-id="4d7ef-139">NOTES</span></span>

## <span data-ttu-id="4d7ef-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d7ef-140">RELATED LINKS</span></span>

[<span data-ttu-id="4d7ef-141">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="4d7ef-141">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)

[<span data-ttu-id="4d7ef-142">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="4d7ef-142">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


