---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
ms.openlocfilehash: a4d28affaa44e96a713adea7935073bcdf9d93c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601574"
---
# <span data-ttu-id="c0a6d-101">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="c0a6d-101">New-AzAutomationCredential</span></span>

## <span data-ttu-id="c0a6d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c0a6d-102">SYNOPSIS</span></span>
<span data-ttu-id="c0a6d-103">Cria uma credencial de automação.</span><span class="sxs-lookup"><span data-stu-id="c0a6d-103">Creates an Automation credential.</span></span>

## <span data-ttu-id="c0a6d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0a6d-104">SYNTAX</span></span>

```
New-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0a6d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c0a6d-105">DESCRIPTION</span></span>
<span data-ttu-id="c0a6d-106">O cmdlet **New-AzAutomationCredential** cria uma credencial como um objeto **PSCredential** na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="c0a6d-106">The **New-AzAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="c0a6d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c0a6d-107">EXAMPLES</span></span>

### <span data-ttu-id="c0a6d-108">Exemplo 1: criar uma credencial</span><span class="sxs-lookup"><span data-stu-id="c0a6d-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c0a6d-109">O primeiro comando atribui um nome de usuário à variável $User.</span><span class="sxs-lookup"><span data-stu-id="c0a6d-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="c0a6d-110">O segundo comando converte uma senha de texto sem formatação em uma cadeia de caracteres segura usando o cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="c0a6d-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="c0a6d-111">O comando armazena esse objeto na variável $Password.</span><span class="sxs-lookup"><span data-stu-id="c0a6d-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="c0a6d-112">O terceiro comando cria uma credencial com base em $User e $Password e, em seguida, armazena-o na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="c0a6d-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="c0a6d-113">O comando final cria uma credencial de automação chamada ContosoCredential que usa $Credential.</span><span class="sxs-lookup"><span data-stu-id="c0a6d-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="c0a6d-114">OS</span><span class="sxs-lookup"><span data-stu-id="c0a6d-114">PARAMETERS</span></span>

### <span data-ttu-id="c0a6d-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c0a6d-115">-AutomationAccountName</span></span>
<span data-ttu-id="c0a6d-116">Especifica o nome da conta de automação na qual esse cmdlet armazena a credencial.</span><span class="sxs-lookup"><span data-stu-id="c0a6d-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="c0a6d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0a6d-117">-DefaultProfile</span></span>
<span data-ttu-id="c0a6d-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c0a6d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0a6d-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="c0a6d-119">-Description</span></span>
<span data-ttu-id="c0a6d-120">Especifica uma descrição para a credencial.</span><span class="sxs-lookup"><span data-stu-id="c0a6d-120">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="c0a6d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c0a6d-121">-Name</span></span>
<span data-ttu-id="c0a6d-122">Especifica um nome para a credencial.</span><span class="sxs-lookup"><span data-stu-id="c0a6d-122">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="c0a6d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0a6d-123">-ResourceGroupName</span></span>
<span data-ttu-id="c0a6d-124">Especifica uma descrição para o grupo de recursos para o qual esse cmdlet cria uma credencial.</span><span class="sxs-lookup"><span data-stu-id="c0a6d-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="c0a6d-125">-Valor</span><span class="sxs-lookup"><span data-stu-id="c0a6d-125">-Value</span></span>
<span data-ttu-id="c0a6d-126">Especifica as credenciais como um objeto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="c0a6d-126">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="c0a6d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0a6d-127">CommonParameters</span></span>
<span data-ttu-id="c0a6d-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0a6d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0a6d-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0a6d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0a6d-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c0a6d-130">INPUTS</span></span>

### <span data-ttu-id="c0a6d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c0a6d-131">System.String</span></span>

### <span data-ttu-id="c0a6d-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="c0a6d-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="c0a6d-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c0a6d-133">OUTPUTS</span></span>

### <span data-ttu-id="c0a6d-134">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="c0a6d-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="c0a6d-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c0a6d-135">NOTES</span></span>

## <span data-ttu-id="c0a6d-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0a6d-136">RELATED LINKS</span></span>

[<span data-ttu-id="c0a6d-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="c0a6d-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="c0a6d-138">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="c0a6d-138">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="c0a6d-139">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="c0a6d-139">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


