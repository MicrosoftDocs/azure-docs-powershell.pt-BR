---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCredential.md
ms.openlocfilehash: e2a461666edf4f06e78f2bc97f47fcb63ab1c19a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428308"
---
# <span data-ttu-id="e0832-101">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e0832-101">Set-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="e0832-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0832-102">SYNOPSIS</span></span>
<span data-ttu-id="e0832-103">Modifica uma credencial de automação.</span><span class="sxs-lookup"><span data-stu-id="e0832-103">Modifies an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0832-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0832-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0832-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e0832-105">DESCRIPTION</span></span>
<span data-ttu-id="e0832-106">O cmdlet **set-AzureRmAutomationCredential** modifica uma credencial como um objeto **PSCredential** na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="e0832-106">The **Set-AzureRmAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="e0832-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e0832-107">EXAMPLES</span></span>

### <span data-ttu-id="e0832-108">Exemplo 1: atualizar uma credencial</span><span class="sxs-lookup"><span data-stu-id="e0832-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="e0832-109">O primeiro comando atribui um nome de usuário à variável $User.</span><span class="sxs-lookup"><span data-stu-id="e0832-109">The first command assigns a user name to the $User variable.</span></span>

<span data-ttu-id="e0832-110">O segundo comando converte uma senha de texto sem formatação em uma cadeia de caracteres segura usando o cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="e0832-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="e0832-111">O comando armazena esse objeto na variável $Password.</span><span class="sxs-lookup"><span data-stu-id="e0832-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="e0832-112">O terceiro comando cria uma credencial com base em $User e $Password e, em seguida, armazena-o na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="e0832-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>

<span data-ttu-id="e0832-113">O comando final modifica a credencial de automação chamada ContosoCredential para usar a credencial em $Credential.</span><span class="sxs-lookup"><span data-stu-id="e0832-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="e0832-114">OS</span><span class="sxs-lookup"><span data-stu-id="e0832-114">PARAMETERS</span></span>

### <span data-ttu-id="e0832-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e0832-115">-AutomationAccountName</span></span>
<span data-ttu-id="e0832-116">Especifica o nome da conta de automação para a qual esse cmdlet modifica uma credencial.</span><span class="sxs-lookup"><span data-stu-id="e0832-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="e0832-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="e0832-117">-Description</span></span>
<span data-ttu-id="e0832-118">Especifica uma descrição para a credencial modificada por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0832-118">Specifies a description for the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e0832-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0832-119">-Name</span></span>
<span data-ttu-id="e0832-120">Especifica o nome da credencial modificada por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0832-120">Specifies the name of the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e0832-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0832-121">-ResourceGroupName</span></span>
<span data-ttu-id="e0832-122">Especifica o nome do grupo de recursos para o qual esse cmdlet modifica uma credencial.</span><span class="sxs-lookup"><span data-stu-id="e0832-122">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="e0832-123">-Valor</span><span class="sxs-lookup"><span data-stu-id="e0832-123">-Value</span></span>
<span data-ttu-id="e0832-124">Especifica as credenciais como um objeto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="e0832-124">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="e0832-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0832-125">-DefaultProfile</span></span>
<span data-ttu-id="e0832-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e0832-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0832-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0832-127">CommonParameters</span></span>
<span data-ttu-id="e0832-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0832-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0832-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0832-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0832-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e0832-130">INPUTS</span></span>

## <span data-ttu-id="e0832-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e0832-131">OUTPUTS</span></span>

### <span data-ttu-id="e0832-132">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="e0832-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="e0832-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e0832-133">NOTES</span></span>

## <span data-ttu-id="e0832-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0832-134">RELATED LINKS</span></span>

[<span data-ttu-id="e0832-135">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e0832-135">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="e0832-136">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e0832-136">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="e0832-137">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e0832-137">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)


