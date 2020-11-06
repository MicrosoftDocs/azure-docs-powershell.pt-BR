---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
ms.openlocfilehash: a72b7dcb729df3327277b2156574c5a0d5d9deb6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426470"
---
# <span data-ttu-id="a49d4-101">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a49d4-101">Get-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="a49d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a49d4-102">SYNOPSIS</span></span>
<span data-ttu-id="a49d4-103">Obtém contas de automação em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a49d4-103">Gets Automation accounts in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a49d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a49d4-104">SYNTAX</span></span>

### <span data-ttu-id="a49d4-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="a49d4-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a49d4-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a49d4-106">ByAutomationAccountName</span></span>
```
Get-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a49d4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a49d4-107">DESCRIPTION</span></span>
<span data-ttu-id="a49d4-108">O cmdlet **Get-AzureRmAutomationAccount** Obtém contas de automação do Azure em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a49d4-108">The **Get-AzureRmAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>
<span data-ttu-id="a49d4-109">Para obter mais informações sobre contas de automação, consulte o cmdlet New-AzureRmAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="a49d4-109">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="a49d4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a49d4-110">EXAMPLES</span></span>

### <span data-ttu-id="a49d4-111">Exemplo 1: obter todas as contas</span><span class="sxs-lookup"><span data-stu-id="a49d4-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="a49d4-112">Esse comando obtém todas as contas de automação no grupo de recursos chamado ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="a49d4-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="a49d4-113">Exemplo 2: obter uma conta</span><span class="sxs-lookup"><span data-stu-id="a49d4-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="a49d4-114">Esse comando obtém a conta de automação chamada ContosoAutomationAccount no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a49d4-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="a49d4-115">OS</span><span class="sxs-lookup"><span data-stu-id="a49d4-115">PARAMETERS</span></span>

### <span data-ttu-id="a49d4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a49d4-116">-DefaultProfile</span></span>
<span data-ttu-id="a49d4-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a49d4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a49d4-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="a49d4-118">-Name</span></span>
<span data-ttu-id="a49d4-119">Especifica o nome da conta de automação obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a49d4-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a49d4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a49d4-120">-ResourceGroupName</span></span>
<span data-ttu-id="a49d4-121">Especifica o nome de um grupo de recursos em que este cmdlet obtém contas de automação.</span><span class="sxs-lookup"><span data-stu-id="a49d4-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

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

### <span data-ttu-id="a49d4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a49d4-122">CommonParameters</span></span>
<span data-ttu-id="a49d4-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a49d4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a49d4-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a49d4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a49d4-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a49d4-125">INPUTS</span></span>

### <span data-ttu-id="a49d4-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a49d4-126">System.String</span></span>

## <span data-ttu-id="a49d4-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a49d4-127">OUTPUTS</span></span>

### <span data-ttu-id="a49d4-128">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a49d4-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="a49d4-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a49d4-129">NOTES</span></span>

## <span data-ttu-id="a49d4-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a49d4-130">RELATED LINKS</span></span>

[<span data-ttu-id="a49d4-131">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a49d4-131">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="a49d4-132">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a49d4-132">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="a49d4-133">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a49d4-133">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


