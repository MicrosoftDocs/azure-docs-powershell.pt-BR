---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
ms.openlocfilehash: a0b23cc5e16a723364d234eb2ee9723f291ee5e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116985"
---
# <span data-ttu-id="02f12-101">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="02f12-101">New-AzAutomationCredential</span></span>

## <span data-ttu-id="02f12-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02f12-102">SYNOPSIS</span></span>
<span data-ttu-id="02f12-103">Cria uma credencial de Automação.</span><span class="sxs-lookup"><span data-stu-id="02f12-103">Creates an Automation credential.</span></span>

## <span data-ttu-id="02f12-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02f12-104">SYNTAX</span></span>

```
New-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="02f12-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="02f12-105">DESCRIPTION</span></span>
<span data-ttu-id="02f12-106">O cmdlet **New-AzAutomationCredential** cria uma credencial como **um objeto PSCredential** no Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="02f12-106">The **New-AzAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="02f12-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="02f12-107">EXAMPLES</span></span>

### <span data-ttu-id="02f12-108">Exemplo 1: Criar uma credencial</span><span class="sxs-lookup"><span data-stu-id="02f12-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="02f12-109">O primeiro comando atribui um nome de usuário à variável $User usuário.</span><span class="sxs-lookup"><span data-stu-id="02f12-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="02f12-110">O segundo comando converte uma senha de texto sem forma em uma cadeia de caracteres segura usando ConvertTo-SecureString cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02f12-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="02f12-111">O comando armazena esse objeto na variável $Password dados.</span><span class="sxs-lookup"><span data-stu-id="02f12-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="02f12-112">O terceiro comando cria uma credencial com base $User e $Password e a armazena na variável $Credential dados.</span><span class="sxs-lookup"><span data-stu-id="02f12-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="02f12-113">O comando final cria uma credencial de Automação chamada ContosoCredential que usa $Credential.</span><span class="sxs-lookup"><span data-stu-id="02f12-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="02f12-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02f12-114">PARAMETERS</span></span>

### <span data-ttu-id="02f12-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="02f12-115">-AutomationAccountName</span></span>
<span data-ttu-id="02f12-116">Especifica o nome da conta automação na qual esse cmdlet armazena a credencial.</span><span class="sxs-lookup"><span data-stu-id="02f12-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="02f12-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02f12-117">-DefaultProfile</span></span>
<span data-ttu-id="02f12-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="02f12-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02f12-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="02f12-119">-Description</span></span>
<span data-ttu-id="02f12-120">Especifica uma descrição para a credencial.</span><span class="sxs-lookup"><span data-stu-id="02f12-120">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="02f12-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="02f12-121">-Name</span></span>
<span data-ttu-id="02f12-122">Especifica um nome para a credencial.</span><span class="sxs-lookup"><span data-stu-id="02f12-122">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="02f12-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02f12-123">-ResourceGroupName</span></span>
<span data-ttu-id="02f12-124">Especifica uma descrição para o grupo de recursos para o qual este cmdlet cria uma credencial.</span><span class="sxs-lookup"><span data-stu-id="02f12-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="02f12-125">-Valor</span><span class="sxs-lookup"><span data-stu-id="02f12-125">-Value</span></span>
<span data-ttu-id="02f12-126">Especifica as credenciais como um **objeto PSCredential.**</span><span class="sxs-lookup"><span data-stu-id="02f12-126">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="02f12-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02f12-127">CommonParameters</span></span>
<span data-ttu-id="02f12-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02f12-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02f12-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02f12-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02f12-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="02f12-130">INPUTS</span></span>

### <span data-ttu-id="02f12-131">System.String</span><span class="sxs-lookup"><span data-stu-id="02f12-131">System.String</span></span>

### <span data-ttu-id="02f12-132">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="02f12-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="02f12-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="02f12-133">OUTPUTS</span></span>

### <span data-ttu-id="02f12-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="02f12-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="02f12-135">Notas</span><span class="sxs-lookup"><span data-stu-id="02f12-135">NOTES</span></span>

## <span data-ttu-id="02f12-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02f12-136">RELATED LINKS</span></span>

[<span data-ttu-id="02f12-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="02f12-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="02f12-138">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="02f12-138">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="02f12-139">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="02f12-139">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


