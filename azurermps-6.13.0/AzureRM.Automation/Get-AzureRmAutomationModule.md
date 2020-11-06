---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
ms.openlocfilehash: 2ed40d0ee0698c8e0ee8d4a1c443db32c843ac65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93601991"
---
# <span data-ttu-id="35cb0-101">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="35cb0-101">Get-AzureRmAutomationModule</span></span>

## <span data-ttu-id="35cb0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35cb0-102">SYNOPSIS</span></span>
<span data-ttu-id="35cb0-103">Obtém metadados para módulos da automação.</span><span class="sxs-lookup"><span data-stu-id="35cb0-103">Gets metadata for modules from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35cb0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35cb0-104">SYNTAX</span></span>

### <span data-ttu-id="35cb0-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="35cb0-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35cb0-106">ByName</span><span class="sxs-lookup"><span data-stu-id="35cb0-106">ByName</span></span>
```
Get-AzureRmAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35cb0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35cb0-107">DESCRIPTION</span></span>
<span data-ttu-id="35cb0-108">O cmdlet **Get-AzureRmAutomationModule** obtém metadados para módulos da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="35cb0-108">The **Get-AzureRmAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="35cb0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35cb0-109">EXAMPLES</span></span>

### <span data-ttu-id="35cb0-110">Exemplo 1: obter todos os módulos</span><span class="sxs-lookup"><span data-stu-id="35cb0-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="35cb0-111">Esse comando obtém todos os módulos na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="35cb0-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="35cb0-112">Exemplo 2: obter um módulo</span><span class="sxs-lookup"><span data-stu-id="35cb0-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="35cb0-113">Esse comando obtém um módulo chamado ContosoModule na conta de automação chamado Contoso17.</span><span class="sxs-lookup"><span data-stu-id="35cb0-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="35cb0-114">OS</span><span class="sxs-lookup"><span data-stu-id="35cb0-114">PARAMETERS</span></span>

### <span data-ttu-id="35cb0-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="35cb0-115">-AutomationAccountName</span></span>
<span data-ttu-id="35cb0-116">Especifica o nome da conta de automação para a qual esse cmdlet obtém metadados de módulo.</span><span class="sxs-lookup"><span data-stu-id="35cb0-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="35cb0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35cb0-117">-DefaultProfile</span></span>
<span data-ttu-id="35cb0-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="35cb0-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35cb0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="35cb0-119">-Name</span></span>
<span data-ttu-id="35cb0-120">Especifica o nome do módulo para o qual esse cmdlet obtém metadados.</span><span class="sxs-lookup"><span data-stu-id="35cb0-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35cb0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35cb0-121">-ResourceGroupName</span></span>
<span data-ttu-id="35cb0-122">Especifica o nome de um grupo de recursos para o qual esse cmdlet obtém metadados de módulo.</span><span class="sxs-lookup"><span data-stu-id="35cb0-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="35cb0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35cb0-123">CommonParameters</span></span>
<span data-ttu-id="35cb0-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35cb0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35cb0-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35cb0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35cb0-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35cb0-126">INPUTS</span></span>

### <span data-ttu-id="35cb0-127">System. String</span><span class="sxs-lookup"><span data-stu-id="35cb0-127">System.String</span></span>

## <span data-ttu-id="35cb0-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35cb0-128">OUTPUTS</span></span>

### <span data-ttu-id="35cb0-129">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="35cb0-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="35cb0-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35cb0-130">NOTES</span></span>

## <span data-ttu-id="35cb0-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35cb0-131">RELATED LINKS</span></span>

[<span data-ttu-id="35cb0-132">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="35cb0-132">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="35cb0-133">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="35cb0-133">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="35cb0-134">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="35cb0-134">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


