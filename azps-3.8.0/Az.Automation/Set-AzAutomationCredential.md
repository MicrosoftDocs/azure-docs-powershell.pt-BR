---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
ms.openlocfilehash: e44b9a5c497aba5533d53acdc9aab31cb5ece703
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777400"
---
# <span data-ttu-id="42290-101">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="42290-101">Set-AzAutomationCredential</span></span>

## <span data-ttu-id="42290-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="42290-102">SYNOPSIS</span></span>
<span data-ttu-id="42290-103">Modifica uma credencial de automação.</span><span class="sxs-lookup"><span data-stu-id="42290-103">Modifies an Automation credential.</span></span>

## <span data-ttu-id="42290-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="42290-104">SYNTAX</span></span>

```
Set-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42290-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="42290-105">DESCRIPTION</span></span>
<span data-ttu-id="42290-106">O cmdlet **set-AzAutomationCredential** modifica uma credencial como um objeto **PSCredential** na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="42290-106">The **Set-AzAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="42290-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="42290-107">EXAMPLES</span></span>

### <span data-ttu-id="42290-108">Exemplo 1: atualizar uma credencial</span><span class="sxs-lookup"><span data-stu-id="42290-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="42290-109">O primeiro comando atribui um nome de usuário à variável $User.</span><span class="sxs-lookup"><span data-stu-id="42290-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="42290-110">O segundo comando converte uma senha de texto sem formatação em uma cadeia de caracteres segura usando o cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="42290-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="42290-111">O comando armazena esse objeto na variável $Password.</span><span class="sxs-lookup"><span data-stu-id="42290-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="42290-112">O terceiro comando cria uma credencial com base em $User e $Password e, em seguida, armazena-o na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="42290-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="42290-113">O comando final modifica a credencial de automação chamada ContosoCredential para usar a credencial em $Credential.</span><span class="sxs-lookup"><span data-stu-id="42290-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="42290-114">OS</span><span class="sxs-lookup"><span data-stu-id="42290-114">PARAMETERS</span></span>

### <span data-ttu-id="42290-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="42290-115">-AutomationAccountName</span></span>
<span data-ttu-id="42290-116">Especifica o nome da conta de automação para a qual esse cmdlet modifica uma credencial.</span><span class="sxs-lookup"><span data-stu-id="42290-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="42290-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42290-117">-DefaultProfile</span></span>
<span data-ttu-id="42290-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="42290-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42290-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="42290-119">-Description</span></span>
<span data-ttu-id="42290-120">Especifica uma descrição para a credencial modificada por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42290-120">Specifies a description for the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="42290-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="42290-121">-Name</span></span>
<span data-ttu-id="42290-122">Especifica o nome da credencial modificada por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42290-122">Specifies the name of the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="42290-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42290-123">-ResourceGroupName</span></span>
<span data-ttu-id="42290-124">Especifica o nome do grupo de recursos para o qual esse cmdlet modifica uma credencial.</span><span class="sxs-lookup"><span data-stu-id="42290-124">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="42290-125">-Valor</span><span class="sxs-lookup"><span data-stu-id="42290-125">-Value</span></span>
<span data-ttu-id="42290-126">Especifica as credenciais como um objeto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="42290-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42290-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42290-127">CommonParameters</span></span>
<span data-ttu-id="42290-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42290-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42290-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42290-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42290-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="42290-130">INPUTS</span></span>

### <span data-ttu-id="42290-131">System. String</span><span class="sxs-lookup"><span data-stu-id="42290-131">System.String</span></span>

### <span data-ttu-id="42290-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="42290-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="42290-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="42290-133">OUTPUTS</span></span>

### <span data-ttu-id="42290-134">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="42290-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="42290-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="42290-135">NOTES</span></span>

## <span data-ttu-id="42290-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42290-136">RELATED LINKS</span></span>

[<span data-ttu-id="42290-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="42290-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="42290-138">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="42290-138">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="42290-139">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="42290-139">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)


