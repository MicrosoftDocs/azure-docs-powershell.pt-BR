---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationConnection.md
ms.openlocfilehash: 6397c1efdce39e575caa98558a54bd279fd0374e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433342"
---
# <span data-ttu-id="903f2-101">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="903f2-101">Get-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="903f2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="903f2-102">SYNOPSIS</span></span>
<span data-ttu-id="903f2-103">Obtém uma conexão de automação.</span><span class="sxs-lookup"><span data-stu-id="903f2-103">Gets an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="903f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="903f2-104">SYNTAX</span></span>

### <span data-ttu-id="903f2-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="903f2-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="903f2-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="903f2-106">ByConnectionName</span></span>
```
Get-AzureRmAutomationConnection [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="903f2-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="903f2-107">ByConnectionTypeName</span></span>
```
Get-AzureRmAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="903f2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="903f2-108">DESCRIPTION</span></span>
<span data-ttu-id="903f2-109">O cmdlet **Get-AzureRmAutomationConnection** Obtém uma ou mais conexões de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="903f2-109">The **Get-AzureRmAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="903f2-110">Por padrão, esse cmdlet recupera todas as conexões.</span><span class="sxs-lookup"><span data-stu-id="903f2-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="903f2-111">Especifique o nome de uma conexão para obter uma conexão específica.</span><span class="sxs-lookup"><span data-stu-id="903f2-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="903f2-112">Especifique o nome do tipo de conexão para obter todas as conexões de um tipo específico.</span><span class="sxs-lookup"><span data-stu-id="903f2-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="903f2-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="903f2-113">EXAMPLES</span></span>

### <span data-ttu-id="903f2-114">Exemplo 1: obter todas as conexões</span><span class="sxs-lookup"><span data-stu-id="903f2-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="903f2-115">Esse comando obtém metadados para todas as conexões na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="903f2-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="903f2-116">Exemplo 2: obter todas as conexões de um tipo</span><span class="sxs-lookup"><span data-stu-id="903f2-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="903f2-117">Esse comando obtém metadados para conexões na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="903f2-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="903f2-118">Este comando obtém conexões do tipo SqlServer.</span><span class="sxs-lookup"><span data-stu-id="903f2-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="903f2-119">Exemplo 3: obter uma conexão</span><span class="sxs-lookup"><span data-stu-id="903f2-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="903f2-120">Esse comando obtém metadados para a conexão chamada ContosoConnection.</span><span class="sxs-lookup"><span data-stu-id="903f2-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="903f2-121">OS</span><span class="sxs-lookup"><span data-stu-id="903f2-121">PARAMETERS</span></span>

### <span data-ttu-id="903f2-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="903f2-122">-AutomationAccountName</span></span>
<span data-ttu-id="903f2-123">Especifica o nome da conta de automação para a qual este cmdlet obtém conexões.</span><span class="sxs-lookup"><span data-stu-id="903f2-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="903f2-124">-ConnectionName</span><span class="sxs-lookup"><span data-stu-id="903f2-124">-ConnectionTypeName</span></span>
<span data-ttu-id="903f2-125">Especifica o nome de um tipo de conexão para o qual esse cmdlet recupera conexões.</span><span class="sxs-lookup"><span data-stu-id="903f2-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

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

### <span data-ttu-id="903f2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="903f2-126">-DefaultProfile</span></span>
<span data-ttu-id="903f2-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="903f2-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="903f2-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="903f2-128">-Name</span></span>
<span data-ttu-id="903f2-129">Especifica o nome de uma conexão que este cmdlet recupera.</span><span class="sxs-lookup"><span data-stu-id="903f2-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

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

### <span data-ttu-id="903f2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="903f2-130">-ResourceGroupName</span></span>
<span data-ttu-id="903f2-131">Especifica o nome de um grupo de recursos para o qual este cmdlet obtém conexões.</span><span class="sxs-lookup"><span data-stu-id="903f2-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="903f2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="903f2-132">CommonParameters</span></span>
<span data-ttu-id="903f2-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="903f2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="903f2-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="903f2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="903f2-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="903f2-135">INPUTS</span></span>

### <span data-ttu-id="903f2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="903f2-136">System.String</span></span>

## <span data-ttu-id="903f2-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="903f2-137">OUTPUTS</span></span>

### <span data-ttu-id="903f2-138">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="903f2-138">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="903f2-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="903f2-139">NOTES</span></span>

## <span data-ttu-id="903f2-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="903f2-140">RELATED LINKS</span></span>

[<span data-ttu-id="903f2-141">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="903f2-141">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)

[<span data-ttu-id="903f2-142">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="903f2-142">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


