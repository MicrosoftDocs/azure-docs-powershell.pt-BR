---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 98d87c060c51d19db45e907f88d39f27350248c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113330"
---
# <span data-ttu-id="a1604-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="a1604-101">New-AzADGroup</span></span>

## <span data-ttu-id="a1604-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1604-102">SYNOPSIS</span></span>
<span data-ttu-id="a1604-103">Cria um novo grupo do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a1604-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="a1604-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1604-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1604-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a1604-105">DESCRIPTION</span></span>
<span data-ttu-id="a1604-106">Cria um novo grupo do Active Directory. Abaixo estão as permissões necessárias:</span><span class="sxs-lookup"><span data-stu-id="a1604-106">Creates a new active directory group.Below are the permissions needed:</span></span>

- <span data-ttu-id="a1604-107">Azure Active Directory Graph</span><span class="sxs-lookup"><span data-stu-id="a1604-107">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="a1604-108">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a1604-108">Directory.ReadWrite.All</span></span>
- <span data-ttu-id="a1604-109">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="a1604-109">Microsoft Graph</span></span>
  - <span data-ttu-id="a1604-110">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a1604-110">Directory.ReadWrite.All</span></span>
  - <span data-ttu-id="a1604-111">PrivilegedAccess.ReadWrite.AzureADGroup</span><span class="sxs-lookup"><span data-stu-id="a1604-111">PrivilegedAccess.ReadWrite.AzureADGroup</span></span>

## <span data-ttu-id="a1604-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a1604-112">EXAMPLES</span></span>

### <span data-ttu-id="a1604-113">Exemplo 1: Criar um novo grupo de AD</span><span class="sxs-lookup"><span data-stu-id="a1604-113">Example 1: Create a new AD group</span></span>

```powershell
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="a1604-114">Cria um novo grupo de AD com o nome "MyGroupDisplayName" e o apelido de email "MyGroupNick".</span><span class="sxs-lookup"><span data-stu-id="a1604-114">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="a1604-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1604-115">PARAMETERS</span></span>

### <span data-ttu-id="a1604-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1604-116">-DefaultProfile</span></span>
<span data-ttu-id="a1604-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1604-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1604-118">-Descrição</span><span class="sxs-lookup"><span data-stu-id="a1604-118">-Description</span></span>
<span data-ttu-id="a1604-119">A descrição do grupo.</span><span class="sxs-lookup"><span data-stu-id="a1604-119">The description for the group.</span></span>

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

### <span data-ttu-id="a1604-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a1604-120">-DisplayName</span></span>
<span data-ttu-id="a1604-121">O nome de exibição do grupo.</span><span class="sxs-lookup"><span data-stu-id="a1604-121">The display name for the group.</span></span>

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

### <span data-ttu-id="a1604-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="a1604-122">-MailNickname</span></span>
<span data-ttu-id="a1604-123">O apelido de email do grupo.</span><span class="sxs-lookup"><span data-stu-id="a1604-123">The mail nickname for the group.</span></span> <span data-ttu-id="a1604-124">Não é possível conter o sinal @.</span><span class="sxs-lookup"><span data-stu-id="a1604-124">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="a1604-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a1604-125">-Confirm</span></span>
<span data-ttu-id="a1604-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1604-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1604-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1604-127">-WhatIf</span></span>
<span data-ttu-id="a1604-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a1604-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1604-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a1604-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1604-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1604-130">CommonParameters</span></span>
<span data-ttu-id="a1604-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1604-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1604-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1604-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1604-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="a1604-133">INPUTS</span></span>

### <span data-ttu-id="a1604-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a1604-134">System.String</span></span>

## <span data-ttu-id="a1604-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="a1604-135">OUTPUTS</span></span>

### <span data-ttu-id="a1604-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="a1604-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="a1604-137">Notas</span><span class="sxs-lookup"><span data-stu-id="a1604-137">NOTES</span></span>

## <span data-ttu-id="a1604-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1604-138">RELATED LINKS</span></span>
