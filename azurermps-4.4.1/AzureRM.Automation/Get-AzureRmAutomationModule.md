---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
ms.openlocfilehash: dcd84c47ff9a6dae06daaf05bde6dd6f4af86553
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431189"
---
# <span data-ttu-id="43594-101">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="43594-101">Get-AzureRmAutomationModule</span></span>

## <span data-ttu-id="43594-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="43594-102">SYNOPSIS</span></span>
<span data-ttu-id="43594-103">Obtém metadados para módulos da automação.</span><span class="sxs-lookup"><span data-stu-id="43594-103">Gets metadata for modules from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43594-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43594-104">SYNTAX</span></span>

### <span data-ttu-id="43594-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="43594-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43594-106">ByName</span><span class="sxs-lookup"><span data-stu-id="43594-106">ByName</span></span>
```
Get-AzureRmAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43594-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="43594-107">DESCRIPTION</span></span>
<span data-ttu-id="43594-108">O cmdlet **Get-AzureRmAutomationModule** obtém metadados para módulos da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="43594-108">The **Get-AzureRmAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="43594-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="43594-109">EXAMPLES</span></span>

### <span data-ttu-id="43594-110">Exemplo 1: obter todos os módulos</span><span class="sxs-lookup"><span data-stu-id="43594-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="43594-111">Esse comando obtém todos os módulos na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="43594-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="43594-112">Exemplo 2: obter um módulo</span><span class="sxs-lookup"><span data-stu-id="43594-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="43594-113">Esse comando obtém um módulo chamado ContosoModule na conta de automação chamado Contoso17.</span><span class="sxs-lookup"><span data-stu-id="43594-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="43594-114">OS</span><span class="sxs-lookup"><span data-stu-id="43594-114">PARAMETERS</span></span>

### <span data-ttu-id="43594-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="43594-115">-AutomationAccountName</span></span>
<span data-ttu-id="43594-116">Especifica o nome da conta de automação para a qual esse cmdlet obtém metadados de módulo.</span><span class="sxs-lookup"><span data-stu-id="43594-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="43594-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="43594-117">-Name</span></span>
<span data-ttu-id="43594-118">Especifica o nome do módulo para o qual esse cmdlet obtém metadados.</span><span class="sxs-lookup"><span data-stu-id="43594-118">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="43594-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43594-119">-ResourceGroupName</span></span>
<span data-ttu-id="43594-120">Especifica o nome de um grupo de recursos para o qual esse cmdlet obtém metadados de módulo.</span><span class="sxs-lookup"><span data-stu-id="43594-120">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="43594-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43594-121">-DefaultProfile</span></span>
<span data-ttu-id="43594-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="43594-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43594-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43594-123">CommonParameters</span></span>
<span data-ttu-id="43594-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43594-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43594-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43594-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43594-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="43594-126">INPUTS</span></span>

## <span data-ttu-id="43594-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="43594-127">OUTPUTS</span></span>

### <span data-ttu-id="43594-128">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="43594-128">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="43594-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="43594-129">NOTES</span></span>

## <span data-ttu-id="43594-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43594-130">RELATED LINKS</span></span>

[<span data-ttu-id="43594-131">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="43594-131">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="43594-132">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="43594-132">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="43594-133">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="43594-133">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


