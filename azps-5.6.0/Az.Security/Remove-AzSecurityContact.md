---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
ms.openlocfilehash: f8b96d8441e9a0b3a5f9b9bc3c775da7d71f12c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890582"
---
# <span data-ttu-id="41d73-101">Remove-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="41d73-101">Remove-AzSecurityContact</span></span>

## <span data-ttu-id="41d73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41d73-102">SYNOPSIS</span></span>
<span data-ttu-id="41d73-103">Exclui um contato de segurança.</span><span class="sxs-lookup"><span data-stu-id="41d73-103">Deletes a security contact.</span></span>

## <span data-ttu-id="41d73-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="41d73-104">SYNTAX</span></span>

### <span data-ttu-id="41d73-105">SubscriptionLevelResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="41d73-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41d73-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="41d73-106">ResourceId</span></span>
```
Remove-AzSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41d73-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="41d73-107">InputObject</span></span>
```
Remove-AzSecurityContact -InputObject <PSSecurityContact> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41d73-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="41d73-108">DESCRIPTION</span></span>
<span data-ttu-id="41d73-109">Exclui um contato de segurança.</span><span class="sxs-lookup"><span data-stu-id="41d73-109">Deletes a security contact.</span></span>

## <span data-ttu-id="41d73-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41d73-110">EXAMPLES</span></span>

### <span data-ttu-id="41d73-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="41d73-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityContact -Name "default1"
```

<span data-ttu-id="41d73-112">Exclui o contato de segurança "padrão1"</span><span class="sxs-lookup"><span data-stu-id="41d73-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="41d73-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="41d73-113">PARAMETERS</span></span>

### <span data-ttu-id="41d73-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41d73-114">-DefaultProfile</span></span>
<span data-ttu-id="41d73-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="41d73-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41d73-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41d73-116">-InputObject</span></span>
<span data-ttu-id="41d73-117">Objeto Input.</span><span class="sxs-lookup"><span data-stu-id="41d73-117">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41d73-118">-Name</span><span class="sxs-lookup"><span data-stu-id="41d73-118">-Name</span></span>
<span data-ttu-id="41d73-119">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="41d73-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41d73-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41d73-120">-PassThru</span></span>
<span data-ttu-id="41d73-121">Retorne se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="41d73-121">Return whether the operation was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41d73-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41d73-122">-ResourceId</span></span>
<span data-ttu-id="41d73-123">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="41d73-123">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41d73-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41d73-124">-Confirm</span></span>
<span data-ttu-id="41d73-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41d73-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41d73-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41d73-126">-WhatIf</span></span>
<span data-ttu-id="41d73-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="41d73-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41d73-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="41d73-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41d73-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41d73-129">CommonParameters</span></span>
<span data-ttu-id="41d73-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41d73-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41d73-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41d73-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41d73-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41d73-132">INPUTS</span></span>

### <span data-ttu-id="41d73-133">System.String</span><span class="sxs-lookup"><span data-stu-id="41d73-133">System.String</span></span>

### <span data-ttu-id="41d73-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="41d73-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="41d73-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="41d73-135">OUTPUTS</span></span>

### <span data-ttu-id="41d73-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="41d73-136">System.Boolean</span></span>

## <span data-ttu-id="41d73-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="41d73-137">NOTES</span></span>

## <span data-ttu-id="41d73-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41d73-138">RELATED LINKS</span></span>
