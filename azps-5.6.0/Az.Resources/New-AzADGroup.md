---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 910453711e047f9be1694bed0c92c502694d8a6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888445"
---
# <span data-ttu-id="24eb0-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="24eb0-101">New-AzADGroup</span></span>

## <span data-ttu-id="24eb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24eb0-102">SYNOPSIS</span></span>
<span data-ttu-id="24eb0-103">Cria um novo grupo do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="24eb0-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="24eb0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="24eb0-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24eb0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="24eb0-105">DESCRIPTION</span></span>
<span data-ttu-id="24eb0-106">Cria um novo grupo do Active Directory. Abaixo estão as permissões necessárias:</span><span class="sxs-lookup"><span data-stu-id="24eb0-106">Creates a new active directory group.Below are the permissions needed:</span></span>

- <span data-ttu-id="24eb0-107">Gráfico do Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="24eb0-107">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="24eb0-108">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="24eb0-108">Directory.ReadWrite.All</span></span>
- <span data-ttu-id="24eb0-109">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="24eb0-109">Microsoft Graph</span></span>
  - <span data-ttu-id="24eb0-110">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="24eb0-110">Directory.ReadWrite.All</span></span>
  - <span data-ttu-id="24eb0-111">PrivilegedAccess.ReadWrite.AzureADGroup</span><span class="sxs-lookup"><span data-stu-id="24eb0-111">PrivilegedAccess.ReadWrite.AzureADGroup</span></span>

## <span data-ttu-id="24eb0-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24eb0-112">EXAMPLES</span></span>

### <span data-ttu-id="24eb0-113">Exemplo 1: Criar um novo grupo de AD</span><span class="sxs-lookup"><span data-stu-id="24eb0-113">Example 1: Create a new AD group</span></span>

```powershell
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="24eb0-114">Cria um novo grupo de AD com o nome "MyGroupDisplayName" e o apelido de email "MyGroupNick".</span><span class="sxs-lookup"><span data-stu-id="24eb0-114">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="24eb0-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="24eb0-115">PARAMETERS</span></span>

### <span data-ttu-id="24eb0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24eb0-116">-DefaultProfile</span></span>
<span data-ttu-id="24eb0-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="24eb0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24eb0-118">-Description</span><span class="sxs-lookup"><span data-stu-id="24eb0-118">-Description</span></span>
<span data-ttu-id="24eb0-119">A descrição do grupo.</span><span class="sxs-lookup"><span data-stu-id="24eb0-119">The description for the group.</span></span>

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

### <span data-ttu-id="24eb0-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="24eb0-120">-DisplayName</span></span>
<span data-ttu-id="24eb0-121">O nome de exibição do grupo.</span><span class="sxs-lookup"><span data-stu-id="24eb0-121">The display name for the group.</span></span>

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

### <span data-ttu-id="24eb0-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="24eb0-122">-MailNickname</span></span>
<span data-ttu-id="24eb0-123">O apelido de email do grupo.</span><span class="sxs-lookup"><span data-stu-id="24eb0-123">The mail nickname for the group.</span></span> <span data-ttu-id="24eb0-124">Não é possível conter o sinal @.</span><span class="sxs-lookup"><span data-stu-id="24eb0-124">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="24eb0-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24eb0-125">-Confirm</span></span>
<span data-ttu-id="24eb0-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24eb0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24eb0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24eb0-127">-WhatIf</span></span>
<span data-ttu-id="24eb0-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="24eb0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24eb0-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="24eb0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24eb0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24eb0-130">CommonParameters</span></span>
<span data-ttu-id="24eb0-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24eb0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24eb0-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24eb0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24eb0-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="24eb0-133">INPUTS</span></span>

### <span data-ttu-id="24eb0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="24eb0-134">System.String</span></span>

## <span data-ttu-id="24eb0-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="24eb0-135">OUTPUTS</span></span>

### <span data-ttu-id="24eb0-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="24eb0-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="24eb0-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="24eb0-137">NOTES</span></span>

## <span data-ttu-id="24eb0-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24eb0-138">RELATED LINKS</span></span>
