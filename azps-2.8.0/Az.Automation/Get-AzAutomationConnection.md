---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
ms.openlocfilehash: 267c18ea4abf87936c47629eca523b254b411240
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597868"
---
# <span data-ttu-id="b4d3d-101">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="b4d3d-101">Get-AzAutomationConnection</span></span>

## <span data-ttu-id="b4d3d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4d3d-102">SYNOPSIS</span></span>
<span data-ttu-id="b4d3d-103">Obtém uma conexão de automação.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-103">Gets an Automation connection.</span></span>

## <span data-ttu-id="b4d3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4d3d-104">SYNTAX</span></span>

### <span data-ttu-id="b4d3d-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="b4d3d-105">ByAll (Default)</span></span>
```
Get-AzAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4d3d-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="b4d3d-106">ByConnectionName</span></span>
```
Get-AzAutomationConnection [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4d3d-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="b4d3d-107">ByConnectionTypeName</span></span>
```
Get-AzAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4d3d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b4d3d-108">DESCRIPTION</span></span>
<span data-ttu-id="b4d3d-109">O cmdlet **Get-AzAutomationConnection** Obtém uma ou mais conexões de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-109">The **Get-AzAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="b4d3d-110">Por padrão, esse cmdlet recupera todas as conexões.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="b4d3d-111">Especifique o nome de uma conexão para obter uma conexão específica.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="b4d3d-112">Especifique o nome do tipo de conexão para obter todas as conexões de um tipo específico.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="b4d3d-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4d3d-113">EXAMPLES</span></span>

### <span data-ttu-id="b4d3d-114">Exemplo 1: obter todas as conexões</span><span class="sxs-lookup"><span data-stu-id="b4d3d-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="b4d3d-115">Esse comando obtém metadados para todas as conexões na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="b4d3d-116">Exemplo 2: obter todas as conexões de um tipo</span><span class="sxs-lookup"><span data-stu-id="b4d3d-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="b4d3d-117">Esse comando obtém metadados para conexões na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="b4d3d-118">Este comando obtém conexões do tipo SqlServer.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="b4d3d-119">Exemplo 3: obter uma conexão</span><span class="sxs-lookup"><span data-stu-id="b4d3d-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="b4d3d-120">Esse comando obtém metadados para a conexão chamada ContosoConnection.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="b4d3d-121">OS</span><span class="sxs-lookup"><span data-stu-id="b4d3d-121">PARAMETERS</span></span>

### <span data-ttu-id="b4d3d-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b4d3d-122">-AutomationAccountName</span></span>
<span data-ttu-id="b4d3d-123">Especifica o nome da conta de automação para a qual este cmdlet obtém conexões.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="b4d3d-124">-ConnectionName</span><span class="sxs-lookup"><span data-stu-id="b4d3d-124">-ConnectionTypeName</span></span>
<span data-ttu-id="b4d3d-125">Especifica o nome de um tipo de conexão para o qual esse cmdlet recupera conexões.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

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

### <span data-ttu-id="b4d3d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4d3d-126">-DefaultProfile</span></span>
<span data-ttu-id="b4d3d-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b4d3d-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4d3d-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4d3d-128">-Name</span></span>
<span data-ttu-id="b4d3d-129">Especifica o nome de uma conexão que este cmdlet recupera.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

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

### <span data-ttu-id="b4d3d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4d3d-130">-ResourceGroupName</span></span>
<span data-ttu-id="b4d3d-131">Especifica o nome de um grupo de recursos para o qual este cmdlet obtém conexões.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="b4d3d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4d3d-132">CommonParameters</span></span>
<span data-ttu-id="b4d3d-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4d3d-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4d3d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4d3d-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b4d3d-135">INPUTS</span></span>

### <span data-ttu-id="b4d3d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b4d3d-136">System.String</span></span>

## <span data-ttu-id="b4d3d-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b4d3d-137">OUTPUTS</span></span>

### <span data-ttu-id="b4d3d-138">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="b4d3d-138">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="b4d3d-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b4d3d-139">NOTES</span></span>

## <span data-ttu-id="b4d3d-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4d3d-140">RELATED LINKS</span></span>

[<span data-ttu-id="b4d3d-141">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="b4d3d-141">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)

[<span data-ttu-id="b4d3d-142">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="b4d3d-142">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


