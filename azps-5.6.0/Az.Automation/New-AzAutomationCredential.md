---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
ms.openlocfilehash: 9858bfdd4aa8388d7e5afa0d2f3ee660bef3a166
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893245"
---
# <span data-ttu-id="d073a-101">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d073a-101">New-AzAutomationCredential</span></span>

## <span data-ttu-id="d073a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d073a-102">SYNOPSIS</span></span>
<span data-ttu-id="d073a-103">Cria uma credencial de automação.</span><span class="sxs-lookup"><span data-stu-id="d073a-103">Creates an Automation credential.</span></span>

## <span data-ttu-id="d073a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d073a-104">SYNTAX</span></span>

```
New-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d073a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d073a-105">DESCRIPTION</span></span>
<span data-ttu-id="d073a-106">O cmdlet **New-AzAutomationCredential** cria uma credencial como um **objeto PSCredential** no Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d073a-106">The **New-AzAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="d073a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d073a-107">EXAMPLES</span></span>

### <span data-ttu-id="d073a-108">Exemplo 1: Criar uma credencial</span><span class="sxs-lookup"><span data-stu-id="d073a-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d073a-109">O primeiro comando atribui um nome de usuário à variável $User de usuário.</span><span class="sxs-lookup"><span data-stu-id="d073a-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="d073a-110">O segundo comando converte uma senha de texto simples em uma cadeia de caracteres segura usando o cmdlet ConvertTo-SecureString de texto.</span><span class="sxs-lookup"><span data-stu-id="d073a-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="d073a-111">O comando armazena esse objeto na variável $Password.</span><span class="sxs-lookup"><span data-stu-id="d073a-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="d073a-112">O terceiro comando cria uma credencial com base $User e $Password e a armazena na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="d073a-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="d073a-113">O comando final cria uma credencial de automação chamada ContosoCredential que usa $Credential.</span><span class="sxs-lookup"><span data-stu-id="d073a-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="d073a-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d073a-114">PARAMETERS</span></span>

### <span data-ttu-id="d073a-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d073a-115">-AutomationAccountName</span></span>
<span data-ttu-id="d073a-116">Especifica o nome da conta de automação na qual esse cmdlet armazena a credencial.</span><span class="sxs-lookup"><span data-stu-id="d073a-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="d073a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d073a-117">-DefaultProfile</span></span>
<span data-ttu-id="d073a-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="d073a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d073a-119">-Description</span><span class="sxs-lookup"><span data-stu-id="d073a-119">-Description</span></span>
<span data-ttu-id="d073a-120">Especifica uma descrição para a credencial.</span><span class="sxs-lookup"><span data-stu-id="d073a-120">Specifies a description for the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d073a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d073a-121">-Name</span></span>
<span data-ttu-id="d073a-122">Especifica um nome para a credencial.</span><span class="sxs-lookup"><span data-stu-id="d073a-122">Specifies a name for the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d073a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d073a-123">-ResourceGroupName</span></span>
<span data-ttu-id="d073a-124">Especifica uma descrição do grupo de recursos para o qual este cmdlet cria uma credencial.</span><span class="sxs-lookup"><span data-stu-id="d073a-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="d073a-125">-Value</span><span class="sxs-lookup"><span data-stu-id="d073a-125">-Value</span></span>
<span data-ttu-id="d073a-126">Especifica as credenciais como um **objeto PSCredential.**</span><span class="sxs-lookup"><span data-stu-id="d073a-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d073a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d073a-127">CommonParameters</span></span>
<span data-ttu-id="d073a-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d073a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d073a-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d073a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d073a-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d073a-130">INPUTS</span></span>

### <span data-ttu-id="d073a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d073a-131">System.String</span></span>

### <span data-ttu-id="d073a-132">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="d073a-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="d073a-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d073a-133">OUTPUTS</span></span>

### <span data-ttu-id="d073a-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="d073a-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="d073a-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="d073a-135">NOTES</span></span>

## <span data-ttu-id="d073a-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d073a-136">RELATED LINKS</span></span>

[<span data-ttu-id="d073a-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d073a-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="d073a-138">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d073a-138">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="d073a-139">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d073a-139">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


