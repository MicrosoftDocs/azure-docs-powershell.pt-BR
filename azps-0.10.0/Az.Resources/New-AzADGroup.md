---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: b5bc2f2eb99a8256dcaa6bc4f026d922f0f563ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776415"
---
# <span data-ttu-id="c87aa-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="c87aa-101">New-AzADGroup</span></span>

## <span data-ttu-id="c87aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c87aa-102">SYNOPSIS</span></span>
<span data-ttu-id="c87aa-103">Cria um novo grupo do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c87aa-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="c87aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c87aa-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c87aa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c87aa-105">DESCRIPTION</span></span>
<span data-ttu-id="c87aa-106">Cria um novo grupo do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c87aa-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="c87aa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c87aa-107">EXAMPLES</span></span>

### <span data-ttu-id="c87aa-108">Exemplo 1-criar um novo grupo de anúncios</span><span class="sxs-lookup"><span data-stu-id="c87aa-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "myemail@domain.com"
```

<span data-ttu-id="c87aa-109">Cria um novo grupo de anúncios com o nome "MyGroupDisplayName" e o apelido do email " myemail@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="c87aa-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "myemail@domain.com".</span></span>

## <span data-ttu-id="c87aa-110">OS</span><span class="sxs-lookup"><span data-stu-id="c87aa-110">PARAMETERS</span></span>

### <span data-ttu-id="c87aa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c87aa-111">-DefaultProfile</span></span>
<span data-ttu-id="c87aa-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c87aa-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c87aa-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c87aa-113">-DisplayName</span></span>
<span data-ttu-id="c87aa-114">O nome de exibição do grupo.</span><span class="sxs-lookup"><span data-stu-id="c87aa-114">The display name for the group.</span></span>

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

### <span data-ttu-id="c87aa-115">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="c87aa-115">-MailNickname</span></span>
<span data-ttu-id="c87aa-116">O apelido do email para o grupo.</span><span class="sxs-lookup"><span data-stu-id="c87aa-116">The mail nickname for the group.</span></span>

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

### <span data-ttu-id="c87aa-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c87aa-117">-Confirm</span></span>
<span data-ttu-id="c87aa-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c87aa-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c87aa-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c87aa-119">-WhatIf</span></span>
<span data-ttu-id="c87aa-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c87aa-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c87aa-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c87aa-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c87aa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c87aa-122">CommonParameters</span></span>
<span data-ttu-id="c87aa-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c87aa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c87aa-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c87aa-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c87aa-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c87aa-125">INPUTS</span></span>

### <span data-ttu-id="c87aa-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c87aa-126">System.String</span></span>

## <span data-ttu-id="c87aa-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c87aa-127">OUTPUTS</span></span>

### <span data-ttu-id="c87aa-128">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="c87aa-128">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="c87aa-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c87aa-129">NOTES</span></span>

## <span data-ttu-id="c87aa-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c87aa-130">RELATED LINKS</span></span>