---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
ms.openlocfilehash: b4cbecd2e29a0b70c7e62194df2364b22b33b462
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118700"
---
# <span data-ttu-id="ca85f-101">Remove-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="ca85f-101">Remove-AzSecurityContact</span></span>

## <span data-ttu-id="ca85f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca85f-102">SYNOPSIS</span></span>
<span data-ttu-id="ca85f-103">Exclui um contato de segurança.</span><span class="sxs-lookup"><span data-stu-id="ca85f-103">Deletes a security contact.</span></span>

## <span data-ttu-id="ca85f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca85f-104">SYNTAX</span></span>

### <span data-ttu-id="ca85f-105">SubscriptionLevelResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ca85f-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca85f-106">Resourceid</span><span class="sxs-lookup"><span data-stu-id="ca85f-106">ResourceId</span></span>
```
Remove-AzSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca85f-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="ca85f-107">InputObject</span></span>
```
Remove-AzSecurityContact -InputObject <PSSecurityContact> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca85f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca85f-108">DESCRIPTION</span></span>
<span data-ttu-id="ca85f-109">Exclui um contato de segurança.</span><span class="sxs-lookup"><span data-stu-id="ca85f-109">Deletes a security contact.</span></span>

## <span data-ttu-id="ca85f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ca85f-110">EXAMPLES</span></span>

### <span data-ttu-id="ca85f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ca85f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityContact -Name "default1"
```

<span data-ttu-id="ca85f-112">Exclui o contato de segurança "padrão1"</span><span class="sxs-lookup"><span data-stu-id="ca85f-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="ca85f-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca85f-113">PARAMETERS</span></span>

### <span data-ttu-id="ca85f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca85f-114">-DefaultProfile</span></span>
<span data-ttu-id="ca85f-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca85f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca85f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca85f-116">-InputObject</span></span>
<span data-ttu-id="ca85f-117">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="ca85f-117">Input Object.</span></span>

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

### <span data-ttu-id="ca85f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca85f-118">-Name</span></span>
<span data-ttu-id="ca85f-119">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ca85f-119">Resource name.</span></span>

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

### <span data-ttu-id="ca85f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca85f-120">-PassThru</span></span>
<span data-ttu-id="ca85f-121">Retorne se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ca85f-121">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="ca85f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca85f-122">-ResourceId</span></span>
<span data-ttu-id="ca85f-123">ID do Recurso.</span><span class="sxs-lookup"><span data-stu-id="ca85f-123">Resource ID.</span></span>

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

### <span data-ttu-id="ca85f-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ca85f-124">-Confirm</span></span>
<span data-ttu-id="ca85f-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca85f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca85f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca85f-126">-WhatIf</span></span>
<span data-ttu-id="ca85f-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ca85f-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca85f-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ca85f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca85f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca85f-129">CommonParameters</span></span>
<span data-ttu-id="ca85f-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca85f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca85f-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca85f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca85f-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="ca85f-132">INPUTS</span></span>

### <span data-ttu-id="ca85f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ca85f-133">System.String</span></span>

### <span data-ttu-id="ca85f-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="ca85f-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="ca85f-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="ca85f-135">OUTPUTS</span></span>

### <span data-ttu-id="ca85f-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ca85f-136">System.Boolean</span></span>

## <span data-ttu-id="ca85f-137">Notas</span><span class="sxs-lookup"><span data-stu-id="ca85f-137">NOTES</span></span>

## <span data-ttu-id="ca85f-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca85f-138">RELATED LINKS</span></span>
