---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
ms.openlocfilehash: cb332c1aed8f828f893417561302ddcf36ba0cdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431181"
---
# <span data-ttu-id="e6d20-101">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e6d20-101">New-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="e6d20-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e6d20-102">SYNOPSIS</span></span>
<span data-ttu-id="e6d20-103">Cria uma credencial de automação.</span><span class="sxs-lookup"><span data-stu-id="e6d20-103">Creates an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6d20-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6d20-104">SYNTAX</span></span>

```
New-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6d20-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e6d20-105">DESCRIPTION</span></span>
<span data-ttu-id="e6d20-106">O cmdlet **New-AzureRmAutomationCredential** cria uma credencial como um objeto **PSCredential** na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="e6d20-106">The **New-AzureRmAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="e6d20-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e6d20-107">EXAMPLES</span></span>

### <span data-ttu-id="e6d20-108">Exemplo 1: criar uma credencial</span><span class="sxs-lookup"><span data-stu-id="e6d20-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e6d20-109">O primeiro comando atribui um nome de usuário à variável $User.</span><span class="sxs-lookup"><span data-stu-id="e6d20-109">The first command assigns a user name to the $User variable.</span></span>

<span data-ttu-id="e6d20-110">O segundo comando converte uma senha de texto sem formatação em uma cadeia de caracteres segura usando o cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="e6d20-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="e6d20-111">O comando armazena esse objeto na variável $Password.</span><span class="sxs-lookup"><span data-stu-id="e6d20-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="e6d20-112">O terceiro comando cria uma credencial com base em $User e $Password e, em seguida, armazena-o na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="e6d20-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>

<span data-ttu-id="e6d20-113">O comando final cria uma credencial de automação chamada ContosoCredential que usa $Credential.</span><span class="sxs-lookup"><span data-stu-id="e6d20-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="e6d20-114">OS</span><span class="sxs-lookup"><span data-stu-id="e6d20-114">PARAMETERS</span></span>

### <span data-ttu-id="e6d20-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e6d20-115">-AutomationAccountName</span></span>
<span data-ttu-id="e6d20-116">Especifica o nome da conta de automação na qual esse cmdlet armazena a credencial.</span><span class="sxs-lookup"><span data-stu-id="e6d20-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="e6d20-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="e6d20-117">-Description</span></span>
<span data-ttu-id="e6d20-118">Especifica uma descrição para a credencial.</span><span class="sxs-lookup"><span data-stu-id="e6d20-118">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="e6d20-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6d20-119">-Name</span></span>
<span data-ttu-id="e6d20-120">Especifica um nome para a credencial.</span><span class="sxs-lookup"><span data-stu-id="e6d20-120">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="e6d20-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6d20-121">-ResourceGroupName</span></span>
<span data-ttu-id="e6d20-122">Especifica uma descrição para o grupo de recursos para o qual esse cmdlet cria uma credencial.</span><span class="sxs-lookup"><span data-stu-id="e6d20-122">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="e6d20-123">-Valor</span><span class="sxs-lookup"><span data-stu-id="e6d20-123">-Value</span></span>
<span data-ttu-id="e6d20-124">Especifica as credenciais como um objeto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="e6d20-124">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="e6d20-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6d20-125">-DefaultProfile</span></span>
<span data-ttu-id="e6d20-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e6d20-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6d20-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6d20-127">CommonParameters</span></span>
<span data-ttu-id="e6d20-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6d20-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6d20-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6d20-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6d20-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e6d20-130">INPUTS</span></span>

## <span data-ttu-id="e6d20-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e6d20-131">OUTPUTS</span></span>

### <span data-ttu-id="e6d20-132">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="e6d20-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="e6d20-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e6d20-133">NOTES</span></span>

## <span data-ttu-id="e6d20-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6d20-134">RELATED LINKS</span></span>

[<span data-ttu-id="e6d20-135">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e6d20-135">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="e6d20-136">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e6d20-136">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)

[<span data-ttu-id="e6d20-137">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e6d20-137">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)

