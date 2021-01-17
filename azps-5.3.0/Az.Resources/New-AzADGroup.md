---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 98d87c060c51d19db45e907f88d39f27350248c9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427276"
---
# <span data-ttu-id="89020-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="89020-101">New-AzADGroup</span></span>

## <span data-ttu-id="89020-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89020-102">SYNOPSIS</span></span>
<span data-ttu-id="89020-103">Cria um novo grupo do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="89020-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="89020-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89020-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89020-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="89020-105">DESCRIPTION</span></span>
<span data-ttu-id="89020-106">Cria um novo grupo do Active Directory. Veja a seguir as permissões necessárias:</span><span class="sxs-lookup"><span data-stu-id="89020-106">Creates a new active directory group.Below are the permissions needed:</span></span>

- <span data-ttu-id="89020-107">Gráfico do Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="89020-107">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="89020-108">Directory. ReadWrite. All</span><span class="sxs-lookup"><span data-stu-id="89020-108">Directory.ReadWrite.All</span></span>
- <span data-ttu-id="89020-109">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="89020-109">Microsoft Graph</span></span>
  - <span data-ttu-id="89020-110">Directory. ReadWrite. All</span><span class="sxs-lookup"><span data-stu-id="89020-110">Directory.ReadWrite.All</span></span>
  - <span data-ttu-id="89020-111">PrivilegedAccess. ReadWrite. AzureADGroup</span><span class="sxs-lookup"><span data-stu-id="89020-111">PrivilegedAccess.ReadWrite.AzureADGroup</span></span>

## <span data-ttu-id="89020-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="89020-112">EXAMPLES</span></span>

### <span data-ttu-id="89020-113">Exemplo 1: criar um novo grupo de anúncios</span><span class="sxs-lookup"><span data-stu-id="89020-113">Example 1: Create a new AD group</span></span>

```powershell
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="89020-114">Cria um novo grupo do AD com o nome "MyGroupDisplayName" e o apelido "MyGroupNick" do email.</span><span class="sxs-lookup"><span data-stu-id="89020-114">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="89020-115">OS</span><span class="sxs-lookup"><span data-stu-id="89020-115">PARAMETERS</span></span>

### <span data-ttu-id="89020-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89020-116">-DefaultProfile</span></span>
<span data-ttu-id="89020-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="89020-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89020-118">-Descrição</span><span class="sxs-lookup"><span data-stu-id="89020-118">-Description</span></span>
<span data-ttu-id="89020-119">A descrição do grupo.</span><span class="sxs-lookup"><span data-stu-id="89020-119">The description for the group.</span></span>

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

### <span data-ttu-id="89020-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="89020-120">-DisplayName</span></span>
<span data-ttu-id="89020-121">O nome de exibição do grupo.</span><span class="sxs-lookup"><span data-stu-id="89020-121">The display name for the group.</span></span>

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

### <span data-ttu-id="89020-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="89020-122">-MailNickname</span></span>
<span data-ttu-id="89020-123">O apelido do email para o grupo.</span><span class="sxs-lookup"><span data-stu-id="89020-123">The mail nickname for the group.</span></span> <span data-ttu-id="89020-124">Não pode conter o sinal @.</span><span class="sxs-lookup"><span data-stu-id="89020-124">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="89020-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="89020-125">-Confirm</span></span>
<span data-ttu-id="89020-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89020-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89020-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89020-127">-WhatIf</span></span>
<span data-ttu-id="89020-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="89020-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89020-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="89020-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89020-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89020-130">CommonParameters</span></span>
<span data-ttu-id="89020-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89020-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89020-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89020-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89020-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="89020-133">INPUTS</span></span>

### <span data-ttu-id="89020-134">System. String</span><span class="sxs-lookup"><span data-stu-id="89020-134">System.String</span></span>

## <span data-ttu-id="89020-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="89020-135">OUTPUTS</span></span>

### <span data-ttu-id="89020-136">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="89020-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="89020-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="89020-137">NOTES</span></span>

## <span data-ttu-id="89020-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89020-138">RELATED LINKS</span></span>
