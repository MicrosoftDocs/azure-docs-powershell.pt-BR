---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C92B4B70-4342-4219-80D3-FB79BDC171A3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 16fbdf1a0a63fb5a75aa7bc200036a7332ea15f8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945831"
---
# <span data-ttu-id="6437b-101">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6437b-101">Set-AzureAutomationCredential</span></span>

## <span data-ttu-id="6437b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6437b-102">SYNOPSIS</span></span>

<span data-ttu-id="6437b-103">Modifica uma credencial na automação.</span><span class="sxs-lookup"><span data-stu-id="6437b-103">Modifies a credential in Automation.</span></span>

## <span data-ttu-id="6437b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6437b-104">SYNTAX</span></span>

```
Set-AzureAutomationCredential -Name <String> [-Description <String>] [-Value <PSCredential>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6437b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6437b-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="6437b-106">O cmdlet **set-AzureAutomationCredential** modifica uma credencial como um objeto **PSCredential** na automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6437b-106">The **Set-AzureAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="6437b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6437b-107">EXAMPLES</span></span>

### <span data-ttu-id="6437b-108">Exemplo 1: atualizar uma credencial</span><span class="sxs-lookup"><span data-stu-id="6437b-108">Example 1: Update a credential</span></span>
```
PS C:\> $user = "MyDomain\MyUser"
PS C:\> $pw = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> $cred = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $user, $pw
PS C:\> New-AzureAutomationCredential -AutomationAccountName "Contos17" -Name "MyCredential" -Value $cred
```

<span data-ttu-id="6437b-109">Esses comandos atualizam uma credencial existente chamada mycredential.</span><span class="sxs-lookup"><span data-stu-id="6437b-109">These commands update an existing credential named MyCredential.</span></span>
<span data-ttu-id="6437b-110">Um objeto Credential é criado pela primeira vez que inclui um nome de usuário e uma senha.</span><span class="sxs-lookup"><span data-stu-id="6437b-110">A credential object is first created that includes a username and password.</span></span>
<span data-ttu-id="6437b-111">Isso é usado no último comando para atualizar a credencial de automação.</span><span class="sxs-lookup"><span data-stu-id="6437b-111">This is then used in the last command to update the automation credential.</span></span>

## <span data-ttu-id="6437b-112">OS</span><span class="sxs-lookup"><span data-stu-id="6437b-112">PARAMETERS</span></span>

### <span data-ttu-id="6437b-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6437b-113">-AutomationAccountName</span></span>
<span data-ttu-id="6437b-114">Especifica o nome da conta de automação com a credencial.</span><span class="sxs-lookup"><span data-stu-id="6437b-114">Specifies the name of the Automation account with the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6437b-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="6437b-115">-Description</span></span>
<span data-ttu-id="6437b-116">Especifica uma descrição para a credencial.</span><span class="sxs-lookup"><span data-stu-id="6437b-116">Specifies a description for the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6437b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="6437b-117">-Name</span></span>
<span data-ttu-id="6437b-118">Especifica o nome da credencial.</span><span class="sxs-lookup"><span data-stu-id="6437b-118">Specifies the name of the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6437b-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="6437b-119">-Profile</span></span>
<span data-ttu-id="6437b-120">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="6437b-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6437b-121">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="6437b-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6437b-122">-Valor</span><span class="sxs-lookup"><span data-stu-id="6437b-122">-Value</span></span>
<span data-ttu-id="6437b-123">Especifica as credenciais como um objeto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="6437b-123">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6437b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6437b-124">CommonParameters</span></span>
<span data-ttu-id="6437b-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6437b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6437b-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6437b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6437b-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6437b-127">INPUTS</span></span>

## <span data-ttu-id="6437b-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6437b-128">OUTPUTS</span></span>

### <span data-ttu-id="6437b-129">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="6437b-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="6437b-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6437b-130">NOTES</span></span>

## <span data-ttu-id="6437b-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6437b-131">RELATED LINKS</span></span>

[<span data-ttu-id="6437b-132">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6437b-132">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="6437b-133">New-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6437b-133">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="6437b-134">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6437b-134">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)


