---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
ms.openlocfilehash: 3cf369be5c7d62d9e4b85002906d55f34a47e40c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954459"
---
# <span data-ttu-id="34571-101">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="34571-101">Get-AzAutomationConnection</span></span>

## <span data-ttu-id="34571-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34571-102">SYNOPSIS</span></span>
<span data-ttu-id="34571-103">Obtém uma conexão de automação.</span><span class="sxs-lookup"><span data-stu-id="34571-103">Gets an Automation connection.</span></span>

## <span data-ttu-id="34571-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34571-104">SYNTAX</span></span>

### <span data-ttu-id="34571-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="34571-105">ByAll (Default)</span></span>
```
Get-AzAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34571-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="34571-106">ByConnectionName</span></span>
```
Get-AzAutomationConnection [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34571-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="34571-107">ByConnectionTypeName</span></span>
```
Get-AzAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34571-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="34571-108">DESCRIPTION</span></span>
<span data-ttu-id="34571-109">O cmdlet **Get-AzAutomationConnection** Obtém uma ou mais conexões de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="34571-109">The **Get-AzAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="34571-110">Por padrão, esse cmdlet recupera todas as conexões.</span><span class="sxs-lookup"><span data-stu-id="34571-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="34571-111">Especifique o nome de uma conexão para obter uma conexão específica.</span><span class="sxs-lookup"><span data-stu-id="34571-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="34571-112">Especifique o nome do tipo de conexão para obter todas as conexões de um tipo específico.</span><span class="sxs-lookup"><span data-stu-id="34571-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="34571-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34571-113">EXAMPLES</span></span>

### <span data-ttu-id="34571-114">Exemplo 1: obter todas as conexões</span><span class="sxs-lookup"><span data-stu-id="34571-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="34571-115">Esse comando obtém metadados para todas as conexões na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="34571-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="34571-116">Exemplo 2: obter todas as conexões de um tipo</span><span class="sxs-lookup"><span data-stu-id="34571-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="34571-117">Esse comando obtém metadados para conexões na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="34571-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="34571-118">Este comando obtém conexões do tipo SqlServer.</span><span class="sxs-lookup"><span data-stu-id="34571-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="34571-119">Exemplo 3: obter uma conexão</span><span class="sxs-lookup"><span data-stu-id="34571-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="34571-120">Esse comando obtém metadados para a conexão chamada ContosoConnection.</span><span class="sxs-lookup"><span data-stu-id="34571-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="34571-121">OS</span><span class="sxs-lookup"><span data-stu-id="34571-121">PARAMETERS</span></span>

### <span data-ttu-id="34571-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="34571-122">-AutomationAccountName</span></span>
<span data-ttu-id="34571-123">Especifica o nome da conta de automação para a qual este cmdlet obtém conexões.</span><span class="sxs-lookup"><span data-stu-id="34571-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="34571-124">-ConnectionName</span><span class="sxs-lookup"><span data-stu-id="34571-124">-ConnectionTypeName</span></span>
<span data-ttu-id="34571-125">Especifica o nome de um tipo de conexão para o qual esse cmdlet recupera conexões.</span><span class="sxs-lookup"><span data-stu-id="34571-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

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

### <span data-ttu-id="34571-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34571-126">-DefaultProfile</span></span>
<span data-ttu-id="34571-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="34571-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34571-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="34571-128">-Name</span></span>
<span data-ttu-id="34571-129">Especifica o nome de uma conexão que este cmdlet recupera.</span><span class="sxs-lookup"><span data-stu-id="34571-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

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

### <span data-ttu-id="34571-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34571-130">-ResourceGroupName</span></span>
<span data-ttu-id="34571-131">Especifica o nome de um grupo de recursos para o qual este cmdlet obtém conexões.</span><span class="sxs-lookup"><span data-stu-id="34571-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="34571-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34571-132">CommonParameters</span></span>
<span data-ttu-id="34571-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34571-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34571-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34571-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34571-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="34571-135">INPUTS</span></span>

### <span data-ttu-id="34571-136">System. String</span><span class="sxs-lookup"><span data-stu-id="34571-136">System.String</span></span>

## <span data-ttu-id="34571-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="34571-137">OUTPUTS</span></span>

### <span data-ttu-id="34571-138">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="34571-138">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="34571-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="34571-139">NOTES</span></span>

## <span data-ttu-id="34571-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34571-140">RELATED LINKS</span></span>

[<span data-ttu-id="34571-141">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="34571-141">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)

[<span data-ttu-id="34571-142">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="34571-142">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


