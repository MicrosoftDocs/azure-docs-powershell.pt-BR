---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 50cb6a806522e8e8b0f3a792ad74e2543633f668
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599406"
---
# <span data-ttu-id="8d5d2-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="8d5d2-101">New-AzADGroup</span></span>

## <span data-ttu-id="8d5d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d5d2-102">SYNOPSIS</span></span>
<span data-ttu-id="8d5d2-103">Cria um novo grupo do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8d5d2-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="8d5d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d5d2-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d5d2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8d5d2-105">DESCRIPTION</span></span>
<span data-ttu-id="8d5d2-106">Cria um novo grupo do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8d5d2-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="8d5d2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d5d2-107">EXAMPLES</span></span>

### <span data-ttu-id="8d5d2-108">Exemplo 1-criar um novo grupo de anúncios</span><span class="sxs-lookup"><span data-stu-id="8d5d2-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="8d5d2-109">Cria um novo grupo do AD com o nome "MyGroupDisplayName" e o apelido "MyGroupNick" do email.</span><span class="sxs-lookup"><span data-stu-id="8d5d2-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="8d5d2-110">OS</span><span class="sxs-lookup"><span data-stu-id="8d5d2-110">PARAMETERS</span></span>

### <span data-ttu-id="8d5d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d5d2-111">-DefaultProfile</span></span>
<span data-ttu-id="8d5d2-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8d5d2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d5d2-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8d5d2-113">-DisplayName</span></span>
<span data-ttu-id="8d5d2-114">O nome de exibição do grupo.</span><span class="sxs-lookup"><span data-stu-id="8d5d2-114">The display name for the group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d5d2-115">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="8d5d2-115">-MailNickname</span></span>
<span data-ttu-id="8d5d2-116">O apelido do email para o grupo.</span><span class="sxs-lookup"><span data-stu-id="8d5d2-116">The mail nickname for the group.</span></span> <span data-ttu-id="8d5d2-117">Não pode conter o sinal @.</span><span class="sxs-lookup"><span data-stu-id="8d5d2-117">Cannot contain the @ sign.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d5d2-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8d5d2-118">-Confirm</span></span>
<span data-ttu-id="8d5d2-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d5d2-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5d2-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d5d2-120">-WhatIf</span></span>
<span data-ttu-id="8d5d2-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8d5d2-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d5d2-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8d5d2-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5d2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d5d2-123">CommonParameters</span></span>
<span data-ttu-id="8d5d2-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d5d2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d5d2-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d5d2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d5d2-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8d5d2-126">INPUTS</span></span>

### <span data-ttu-id="8d5d2-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8d5d2-127">System.String</span></span>

## <span data-ttu-id="8d5d2-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8d5d2-128">OUTPUTS</span></span>

### <span data-ttu-id="8d5d2-129">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="8d5d2-129">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="8d5d2-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8d5d2-130">NOTES</span></span>

## <span data-ttu-id="8d5d2-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d5d2-131">RELATED LINKS</span></span>
