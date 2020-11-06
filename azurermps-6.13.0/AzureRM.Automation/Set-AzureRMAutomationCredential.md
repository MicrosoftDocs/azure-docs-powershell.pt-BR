---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCredential.md
ms.openlocfilehash: a05662917d7e29f090867b0c91503292a9bc917e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427308"
---
# <span data-ttu-id="5c013-101">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5c013-101">Set-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="5c013-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5c013-102">SYNOPSIS</span></span>
<span data-ttu-id="5c013-103">Modifica uma credencial de automação.</span><span class="sxs-lookup"><span data-stu-id="5c013-103">Modifies an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c013-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c013-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c013-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5c013-105">DESCRIPTION</span></span>
<span data-ttu-id="5c013-106">O cmdlet **set-AzureRmAutomationCredential** modifica uma credencial como um objeto **PSCredential** na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="5c013-106">The **Set-AzureRmAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="5c013-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5c013-107">EXAMPLES</span></span>

### <span data-ttu-id="5c013-108">Exemplo 1: atualizar uma credencial</span><span class="sxs-lookup"><span data-stu-id="5c013-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="5c013-109">O primeiro comando atribui um nome de usuário à variável $User.</span><span class="sxs-lookup"><span data-stu-id="5c013-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="5c013-110">O segundo comando converte uma senha de texto sem formatação em uma cadeia de caracteres segura usando o cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="5c013-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="5c013-111">O comando armazena esse objeto na variável $Password.</span><span class="sxs-lookup"><span data-stu-id="5c013-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="5c013-112">O terceiro comando cria uma credencial com base em $User e $Password e, em seguida, armazena-o na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="5c013-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="5c013-113">O comando final modifica a credencial de automação chamada ContosoCredential para usar a credencial em $Credential.</span><span class="sxs-lookup"><span data-stu-id="5c013-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="5c013-114">OS</span><span class="sxs-lookup"><span data-stu-id="5c013-114">PARAMETERS</span></span>

### <span data-ttu-id="5c013-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5c013-115">-AutomationAccountName</span></span>
<span data-ttu-id="5c013-116">Especifica o nome da conta de automação para a qual esse cmdlet modifica uma credencial.</span><span class="sxs-lookup"><span data-stu-id="5c013-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="5c013-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c013-117">-DefaultProfile</span></span>
<span data-ttu-id="5c013-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5c013-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c013-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="5c013-119">-Description</span></span>
<span data-ttu-id="5c013-120">Especifica uma descrição para a credencial modificada por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c013-120">Specifies a description for the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5c013-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="5c013-121">-Name</span></span>
<span data-ttu-id="5c013-122">Especifica o nome da credencial modificada por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c013-122">Specifies the name of the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5c013-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c013-123">-ResourceGroupName</span></span>
<span data-ttu-id="5c013-124">Especifica o nome do grupo de recursos para o qual esse cmdlet modifica uma credencial.</span><span class="sxs-lookup"><span data-stu-id="5c013-124">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="5c013-125">-Valor</span><span class="sxs-lookup"><span data-stu-id="5c013-125">-Value</span></span>
<span data-ttu-id="5c013-126">Especifica as credenciais como um objeto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="5c013-126">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="5c013-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c013-127">CommonParameters</span></span>
<span data-ttu-id="5c013-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c013-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c013-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c013-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c013-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5c013-130">INPUTS</span></span>

### <span data-ttu-id="5c013-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5c013-131">System.String</span></span>

### <span data-ttu-id="5c013-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="5c013-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="5c013-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5c013-133">OUTPUTS</span></span>

### <span data-ttu-id="5c013-134">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="5c013-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="5c013-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5c013-135">NOTES</span></span>

## <span data-ttu-id="5c013-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5c013-136">RELATED LINKS</span></span>

[<span data-ttu-id="5c013-137">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5c013-137">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="5c013-138">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5c013-138">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="5c013-139">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5c013-139">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)


