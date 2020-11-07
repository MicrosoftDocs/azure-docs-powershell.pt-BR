---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: DDEBA3E1-B5A3-4F16-9A67-A95D15851A33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0899349c3dbfa368b3ce0dbb4d4085c3ea527c43
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946492"
---
# <span data-ttu-id="00bc7-101">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="00bc7-101">Remove-AzureAutomationConnection</span></span>

## <span data-ttu-id="00bc7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="00bc7-102">SYNOPSIS</span></span>

<span data-ttu-id="00bc7-103">Remove uma conexão de automação.</span><span class="sxs-lookup"><span data-stu-id="00bc7-103">Removes a connection from Automation.</span></span>

## <span data-ttu-id="00bc7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00bc7-104">SYNTAX</span></span>

```
Remove-AzureAutomationConnection -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="00bc7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="00bc7-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="00bc7-106">O cmdlet **Remove-AzureAutomationConnection** remove uma conexão da automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="00bc7-106">The **Remove-AzureAutomationConnection** cmdlet removes a connection from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="00bc7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="00bc7-107">EXAMPLES</span></span>

### <span data-ttu-id="00bc7-108">Exemplo 1: remover uma conexão</span><span class="sxs-lookup"><span data-stu-id="00bc7-108">Example 1: Remove a connection</span></span>
```
PS C:\> Remove-AzureAutomationConnection -AutomationAccountName "Contoso17" -Name "MyConnection"
```

<span data-ttu-id="00bc7-109">Esse comando Remove um certificado denominado MyConnection na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="00bc7-109">This command removes a certificate named MyConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="00bc7-110">OS</span><span class="sxs-lookup"><span data-stu-id="00bc7-110">PARAMETERS</span></span>

### <span data-ttu-id="00bc7-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="00bc7-111">-AutomationAccountName</span></span>
<span data-ttu-id="00bc7-112">Especifica o nome da conta de automação com a credencial.</span><span class="sxs-lookup"><span data-stu-id="00bc7-112">Specifies the name of the Automation account with the credential.</span></span>

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

### <span data-ttu-id="00bc7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="00bc7-113">-Force</span></span>
<span data-ttu-id="00bc7-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="00bc7-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00bc7-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="00bc7-115">-Name</span></span>
<span data-ttu-id="00bc7-116">Especifica o nome da conexão.</span><span class="sxs-lookup"><span data-stu-id="00bc7-116">Specifies the name of the connection.</span></span>

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

### <span data-ttu-id="00bc7-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="00bc7-117">-Profile</span></span>
<span data-ttu-id="00bc7-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="00bc7-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="00bc7-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="00bc7-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="00bc7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00bc7-120">CommonParameters</span></span>
<span data-ttu-id="00bc7-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00bc7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00bc7-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00bc7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00bc7-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="00bc7-123">INPUTS</span></span>

## <span data-ttu-id="00bc7-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="00bc7-124">OUTPUTS</span></span>

## <span data-ttu-id="00bc7-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="00bc7-125">NOTES</span></span>

## <span data-ttu-id="00bc7-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00bc7-126">RELATED LINKS</span></span>

[<span data-ttu-id="00bc7-127">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="00bc7-127">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="00bc7-128">New-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="00bc7-128">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="00bc7-129">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="00bc7-129">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


