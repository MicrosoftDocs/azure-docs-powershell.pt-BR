---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
ms.openlocfilehash: d79f46e645bb5889c58aaca4b3fbdd046be5c756
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603409"
---
# <span data-ttu-id="ac3c6-101">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ac3c6-101">Get-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="ac3c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ac3c6-102">SYNOPSIS</span></span>
<span data-ttu-id="ac3c6-103">Obtém contas de automação em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ac3c6-103">Gets Automation accounts in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac3c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac3c6-104">SYNTAX</span></span>

### <span data-ttu-id="ac3c6-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="ac3c6-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac3c6-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ac3c6-106">ByAutomationAccountName</span></span>
```
Get-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac3c6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ac3c6-107">DESCRIPTION</span></span>
<span data-ttu-id="ac3c6-108">O cmdlet **Get-AzureRmAutomationAccount** Obtém contas de automação do Azure em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ac3c6-108">The **Get-AzureRmAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>

<span data-ttu-id="ac3c6-109">Para obter mais informações sobre contas de automação, consulte o cmdlet New-AzureRmAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="ac3c6-109">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="ac3c6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ac3c6-110">EXAMPLES</span></span>

### <span data-ttu-id="ac3c6-111">Exemplo 1: obter todas as contas</span><span class="sxs-lookup"><span data-stu-id="ac3c6-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="ac3c6-112">Esse comando obtém todas as contas de automação no grupo de recursos chamado ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="ac3c6-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="ac3c6-113">Exemplo 2: obter uma conta</span><span class="sxs-lookup"><span data-stu-id="ac3c6-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="ac3c6-114">Esse comando obtém a conta de automação chamada ContosoAutomationAccount no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ac3c6-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="ac3c6-115">OS</span><span class="sxs-lookup"><span data-stu-id="ac3c6-115">PARAMETERS</span></span>

### <span data-ttu-id="ac3c6-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac3c6-116">-Name</span></span>
<span data-ttu-id="ac3c6-117">Especifica o nome da conta de automação obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac3c6-117">Specifies the name of the Automation account that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac3c6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac3c6-118">-ResourceGroupName</span></span>
<span data-ttu-id="ac3c6-119">Especifica o nome de um grupo de recursos em que este cmdlet obtém contas de automação.</span><span class="sxs-lookup"><span data-stu-id="ac3c6-119">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac3c6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac3c6-120">-DefaultProfile</span></span>
<span data-ttu-id="ac3c6-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ac3c6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac3c6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac3c6-122">CommonParameters</span></span>
<span data-ttu-id="ac3c6-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac3c6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac3c6-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac3c6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac3c6-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ac3c6-125">INPUTS</span></span>

## <span data-ttu-id="ac3c6-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ac3c6-126">OUTPUTS</span></span>

### <span data-ttu-id="ac3c6-127">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ac3c6-127">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="ac3c6-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ac3c6-128">NOTES</span></span>

## <span data-ttu-id="ac3c6-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ac3c6-129">RELATED LINKS</span></span>

[<span data-ttu-id="ac3c6-130">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ac3c6-130">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="ac3c6-131">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ac3c6-131">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="ac3c6-132">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ac3c6-132">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


