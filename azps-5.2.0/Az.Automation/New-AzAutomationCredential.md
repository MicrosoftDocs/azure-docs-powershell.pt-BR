---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
ms.openlocfilehash: a0b23cc5e16a723364d234eb2ee9723f291ee5e4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264561"
---
# <span data-ttu-id="9d745-101">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="9d745-101">New-AzAutomationCredential</span></span>

## <span data-ttu-id="9d745-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9d745-102">SYNOPSIS</span></span>
<span data-ttu-id="9d745-103">Cria uma credencial de automação.</span><span class="sxs-lookup"><span data-stu-id="9d745-103">Creates an Automation credential.</span></span>

## <span data-ttu-id="9d745-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d745-104">SYNTAX</span></span>

```
New-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d745-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9d745-105">DESCRIPTION</span></span>
<span data-ttu-id="9d745-106">O cmdlet **New-AzAutomationCredential** cria uma credencial como um objeto **PSCredential** na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="9d745-106">The **New-AzAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="9d745-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d745-107">EXAMPLES</span></span>

### <span data-ttu-id="9d745-108">Exemplo 1: criar uma credencial</span><span class="sxs-lookup"><span data-stu-id="9d745-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9d745-109">O primeiro comando atribui um nome de usuário à variável $User.</span><span class="sxs-lookup"><span data-stu-id="9d745-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="9d745-110">O segundo comando converte uma senha de texto sem formatação em uma cadeia de caracteres segura usando o cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="9d745-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="9d745-111">O comando armazena esse objeto na variável $Password.</span><span class="sxs-lookup"><span data-stu-id="9d745-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="9d745-112">O terceiro comando cria uma credencial com base em $User e $Password e, em seguida, armazena-o na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="9d745-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="9d745-113">O comando final cria uma credencial de automação chamada ContosoCredential que usa $Credential.</span><span class="sxs-lookup"><span data-stu-id="9d745-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="9d745-114">OS</span><span class="sxs-lookup"><span data-stu-id="9d745-114">PARAMETERS</span></span>

### <span data-ttu-id="9d745-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9d745-115">-AutomationAccountName</span></span>
<span data-ttu-id="9d745-116">Especifica o nome da conta de automação na qual esse cmdlet armazena a credencial.</span><span class="sxs-lookup"><span data-stu-id="9d745-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="9d745-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d745-117">-DefaultProfile</span></span>
<span data-ttu-id="9d745-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9d745-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d745-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="9d745-119">-Description</span></span>
<span data-ttu-id="9d745-120">Especifica uma descrição para a credencial.</span><span class="sxs-lookup"><span data-stu-id="9d745-120">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="9d745-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d745-121">-Name</span></span>
<span data-ttu-id="9d745-122">Especifica um nome para a credencial.</span><span class="sxs-lookup"><span data-stu-id="9d745-122">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="9d745-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d745-123">-ResourceGroupName</span></span>
<span data-ttu-id="9d745-124">Especifica uma descrição para o grupo de recursos para o qual esse cmdlet cria uma credencial.</span><span class="sxs-lookup"><span data-stu-id="9d745-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="9d745-125">-Valor</span><span class="sxs-lookup"><span data-stu-id="9d745-125">-Value</span></span>
<span data-ttu-id="9d745-126">Especifica as credenciais como um objeto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="9d745-126">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="9d745-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d745-127">CommonParameters</span></span>
<span data-ttu-id="9d745-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d745-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d745-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d745-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d745-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9d745-130">INPUTS</span></span>

### <span data-ttu-id="9d745-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9d745-131">System.String</span></span>

### <span data-ttu-id="9d745-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="9d745-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="9d745-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9d745-133">OUTPUTS</span></span>

### <span data-ttu-id="9d745-134">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="9d745-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="9d745-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9d745-135">NOTES</span></span>

## <span data-ttu-id="9d745-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d745-136">RELATED LINKS</span></span>

[<span data-ttu-id="9d745-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="9d745-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="9d745-138">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="9d745-138">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="9d745-139">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="9d745-139">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


