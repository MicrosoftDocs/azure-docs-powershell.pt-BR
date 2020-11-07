---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: BCF8DAB4-3E14-463B-A18F-E91C740B0D3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 08dd82489bf02efa167386300b9b1d565e1a63de
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946493"
---
# <span data-ttu-id="a4a6b-101">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a4a6b-101">Remove-AzureAutomationCertificate</span></span>

## <span data-ttu-id="a4a6b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a4a6b-102">SYNOPSIS</span></span>

<span data-ttu-id="a4a6b-103">Remove um certificado de automação.</span><span class="sxs-lookup"><span data-stu-id="a4a6b-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="a4a6b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4a6b-104">SYNTAX</span></span>

```
Remove-AzureAutomationCertificate -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a4a6b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a4a6b-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="a4a6b-106">O cmdlet **Remove-AzureAutomationAccount** remove um certificado da automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a4a6b-106">The **Remove-AzureAutomationAccount** cmdlet removes a certificate from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="a4a6b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a4a6b-107">EXAMPLES</span></span>

### <span data-ttu-id="a4a6b-108">Exemplo 1: remover um certificado</span><span class="sxs-lookup"><span data-stu-id="a4a6b-108">Example 1: Remove a certificate</span></span>
```
PS C:\> Remove-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01"
```

<span data-ttu-id="a4a6b-109">Esse comando Remove um certificado denominado Cert01 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a4a6b-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a4a6b-110">OS</span><span class="sxs-lookup"><span data-stu-id="a4a6b-110">PARAMETERS</span></span>

### <span data-ttu-id="a4a6b-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a4a6b-111">-AutomationAccountName</span></span>
<span data-ttu-id="a4a6b-112">Especifica o nome da conta de automação com o certificado.</span><span class="sxs-lookup"><span data-stu-id="a4a6b-112">Specifies the name of the Automation account with the certificate.</span></span>

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

### <span data-ttu-id="a4a6b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a4a6b-113">-Force</span></span>
<span data-ttu-id="a4a6b-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a4a6b-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a4a6b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4a6b-115">-Name</span></span>
<span data-ttu-id="a4a6b-116">Especifica o nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="a4a6b-116">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="a4a6b-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="a4a6b-117">-Profile</span></span>
<span data-ttu-id="a4a6b-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="a4a6b-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a4a6b-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="a4a6b-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a4a6b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4a6b-120">CommonParameters</span></span>
<span data-ttu-id="a4a6b-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4a6b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4a6b-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4a6b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4a6b-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a4a6b-123">INPUTS</span></span>

## <span data-ttu-id="a4a6b-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a4a6b-124">OUTPUTS</span></span>

## <span data-ttu-id="a4a6b-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a4a6b-125">NOTES</span></span>

## <span data-ttu-id="a4a6b-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a4a6b-126">RELATED LINKS</span></span>

[<span data-ttu-id="a4a6b-127">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a4a6b-127">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="a4a6b-128">New-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a4a6b-128">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="a4a6b-129">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a4a6b-129">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


