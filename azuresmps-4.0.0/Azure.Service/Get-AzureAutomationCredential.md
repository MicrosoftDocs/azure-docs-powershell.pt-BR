---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C69558DB-78C3-4162-99C3-1300C3FE5287
online version: ''
schema: 2.0.0
ms.openlocfilehash: aa73cf467ffc3675b17b6c59ef5bd07483803267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945659"
---
# <span data-ttu-id="aac07-101">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="aac07-101">Get-AzureAutomationCredential</span></span>

## <span data-ttu-id="aac07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aac07-102">SYNOPSIS</span></span>

<span data-ttu-id="aac07-103">Obtém uma credencial de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="aac07-103">Gets an Azure Automation credential.</span></span>

## <span data-ttu-id="aac07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aac07-104">SYNTAX</span></span>

### <span data-ttu-id="aac07-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="aac07-105">ByAll (Default)</span></span>
```
Get-AzureAutomationCredential -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="aac07-106">ByName</span><span class="sxs-lookup"><span data-stu-id="aac07-106">ByName</span></span>
```
Get-AzureAutomationCredential -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="aac07-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aac07-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="aac07-108">O cmdlet **Get-AzureAutomationCredential** Obtém uma ou mais credenciais de automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aac07-108">The **Get-AzureAutomationCredential** cmdlet gets one or more Microsoft Azure Automation credentials.</span></span>
<span data-ttu-id="aac07-109">Por padrão, todas as credenciais são retornadas.</span><span class="sxs-lookup"><span data-stu-id="aac07-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="aac07-110">Para obter uma credencial específica, especifique o nome dela.</span><span class="sxs-lookup"><span data-stu-id="aac07-110">To get a specific credential, specify its name.</span></span>

## <span data-ttu-id="aac07-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aac07-111">EXAMPLES</span></span>

### <span data-ttu-id="aac07-112">Exemplo 1: obter todas as credenciais</span><span class="sxs-lookup"><span data-stu-id="aac07-112">Example 1: Get all credentials</span></span>
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17"
```

<span data-ttu-id="aac07-113">Esse comando obtém todas as credenciais na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="aac07-113">This command gets all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="aac07-114">Exemplo 2: obter uma credencial</span><span class="sxs-lookup"><span data-stu-id="aac07-114">Example 2: Get a credential</span></span>
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential"
```

<span data-ttu-id="aac07-115">Esse comando obtém a credencial chamada mycredential.</span><span class="sxs-lookup"><span data-stu-id="aac07-115">This command gets the credential named MyCredential.</span></span>

## <span data-ttu-id="aac07-116">OS</span><span class="sxs-lookup"><span data-stu-id="aac07-116">PARAMETERS</span></span>

### <span data-ttu-id="aac07-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="aac07-117">-AutomationAccountName</span></span>
<span data-ttu-id="aac07-118">Especifica o nome da conta de automação com a credencial a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="aac07-118">Specifies the name of the automation account with the credential to retrieve.</span></span>

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

### <span data-ttu-id="aac07-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="aac07-119">-Name</span></span>
<span data-ttu-id="aac07-120">Especifica o nome de uma credencial a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="aac07-120">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aac07-121">-Perfil</span><span class="sxs-lookup"><span data-stu-id="aac07-121">-Profile</span></span>
<span data-ttu-id="aac07-122">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="aac07-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="aac07-123">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="aac07-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="aac07-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aac07-124">CommonParameters</span></span>
<span data-ttu-id="aac07-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aac07-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aac07-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aac07-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aac07-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aac07-127">INPUTS</span></span>

## <span data-ttu-id="aac07-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aac07-128">OUTPUTS</span></span>

### <span data-ttu-id="aac07-129">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="aac07-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="aac07-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aac07-130">NOTES</span></span>

## <span data-ttu-id="aac07-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aac07-131">RELATED LINKS</span></span>

[<span data-ttu-id="aac07-132">New-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="aac07-132">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="aac07-133">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="aac07-133">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)

[<span data-ttu-id="aac07-134">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="aac07-134">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


