---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: E42F05D0-28AD-4772-9F53-BCE6EFC698AF
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc7d44b87c1e371f0d0c065746dae991cff1cca8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946221"
---
# <span data-ttu-id="12444-101">New-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="12444-101">New-AzureAutomationCredential</span></span>

## <span data-ttu-id="12444-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12444-102">SYNOPSIS</span></span>

<span data-ttu-id="12444-103">Cria uma credencial na automação.</span><span class="sxs-lookup"><span data-stu-id="12444-103">Creates a credential in Automation.</span></span>

## <span data-ttu-id="12444-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12444-104">SYNTAX</span></span>

```
New-AzureAutomationCredential -Name <String> [-Description <String>] -Value <PSCredential>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="12444-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12444-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="12444-106">O cmdlet **New-AzureAutomationCredential** cria uma credencial como um objeto **PSCredential** na automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="12444-106">The **New-AzureAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="12444-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12444-107">EXAMPLES</span></span>

### <span data-ttu-id="12444-108">Exemplo 1: criar uma credencial</span><span class="sxs-lookup"><span data-stu-id="12444-108">Example 1: Create a credential</span></span>
```
PS C:\> $user = "MyDomain\MyUser"
PS C:\> $pw = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> $cred = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $user, $pw
PS C:\> New-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential" -Value $cred
```

<span data-ttu-id="12444-109">Esses comandos criam uma credencial chamada mycredential.</span><span class="sxs-lookup"><span data-stu-id="12444-109">These commands create a credential named MyCredential.</span></span>
<span data-ttu-id="12444-110">Um objeto Credential é criado pela primeira vez que inclui um nome de usuário e uma senha.</span><span class="sxs-lookup"><span data-stu-id="12444-110">A credential object is first created that includes a username and password.</span></span>
<span data-ttu-id="12444-111">Isso é usado no último comando para criar a credencial de automação.</span><span class="sxs-lookup"><span data-stu-id="12444-111">This is then used in the last command to create the Automation credential.</span></span>

## <span data-ttu-id="12444-112">OS</span><span class="sxs-lookup"><span data-stu-id="12444-112">PARAMETERS</span></span>

### <span data-ttu-id="12444-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="12444-113">-AutomationAccountName</span></span>
<span data-ttu-id="12444-114">Especifica o nome da conta de automação na qual a credencial será armazenada.</span><span class="sxs-lookup"><span data-stu-id="12444-114">Specifies the name of the Automation account the credential will be stored in.</span></span>

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

### <span data-ttu-id="12444-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="12444-115">-Description</span></span>
<span data-ttu-id="12444-116">Especifica uma descrição para a credencial.</span><span class="sxs-lookup"><span data-stu-id="12444-116">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="12444-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="12444-117">-Name</span></span>
<span data-ttu-id="12444-118">Especifica um nome para a credencial.</span><span class="sxs-lookup"><span data-stu-id="12444-118">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="12444-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="12444-119">-Profile</span></span>
<span data-ttu-id="12444-120">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="12444-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="12444-121">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="12444-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="12444-122">-Valor</span><span class="sxs-lookup"><span data-stu-id="12444-122">-Value</span></span>
<span data-ttu-id="12444-123">Especifica as credenciais como um objeto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="12444-123">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12444-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12444-124">CommonParameters</span></span>
<span data-ttu-id="12444-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12444-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12444-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12444-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12444-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12444-127">INPUTS</span></span>

## <span data-ttu-id="12444-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12444-128">OUTPUTS</span></span>

### <span data-ttu-id="12444-129">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="12444-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="12444-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12444-130">NOTES</span></span>

## <span data-ttu-id="12444-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12444-131">RELATED LINKS</span></span>

[<span data-ttu-id="12444-132">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="12444-132">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="12444-133">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="12444-133">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)

[<span data-ttu-id="12444-134">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="12444-134">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


