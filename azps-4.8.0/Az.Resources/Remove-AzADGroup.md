---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
ms.openlocfilehash: d066e36b4430f865143a8e8ee14693c38054f02c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113344"
---
# <span data-ttu-id="582b1-101">Remove-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="582b1-101">Remove-AzADGroup</span></span>

## <span data-ttu-id="582b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="582b1-102">SYNOPSIS</span></span>
<span data-ttu-id="582b1-103">Exclui um grupo do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="582b1-103">Deletes an active directory group.</span></span>

## <span data-ttu-id="582b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="582b1-104">SYNTAX</span></span>

### <span data-ttu-id="582b1-105">ObjectIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="582b1-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADGroup -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="582b1-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="582b1-106">DisplayNameParameterSet</span></span>
```
Remove-AzADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="582b1-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="582b1-107">InputObjectParameterSet</span></span>
```
Remove-AzADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="582b1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="582b1-108">DESCRIPTION</span></span>
<span data-ttu-id="582b1-109">Exclui um grupo do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="582b1-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="582b1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="582b1-110">EXAMPLES</span></span>

### <span data-ttu-id="582b1-111">Exemplo 1: remover um grupo por ID de objeto</span><span class="sxs-lookup"><span data-stu-id="582b1-111">Example 1: Remove a group by object id</span></span>

```powershell
PS C:\> Remove-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="582b1-112">Remove o grupo com a ID de objeto "85F89C90-780E-4AA6-9F4F-6F268D322EEE" do locatário.</span><span class="sxs-lookup"><span data-stu-id="582b1-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="582b1-113">Exemplo 2: remover um grupo por tubulação</span><span class="sxs-lookup"><span data-stu-id="582b1-113">Example 2: Remove a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroup
```

<span data-ttu-id="582b1-114">Obtém o grupo com a ID de objeto ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' e canaliza-se para Remove-AzADGroup para remover o grupo do locatário.</span><span class="sxs-lookup"><span data-stu-id="582b1-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="582b1-115">OS</span><span class="sxs-lookup"><span data-stu-id="582b1-115">PARAMETERS</span></span>

### <span data-ttu-id="582b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="582b1-116">-DefaultProfile</span></span>
<span data-ttu-id="582b1-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="582b1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="582b1-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="582b1-118">-DisplayName</span></span>
<span data-ttu-id="582b1-119">O nome de exibição do grupo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="582b1-119">The display name of the group to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="582b1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="582b1-120">-Force</span></span>
<span data-ttu-id="582b1-121">Se especificado, não pede confirmação para excluir o grupo.</span><span class="sxs-lookup"><span data-stu-id="582b1-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

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

### <span data-ttu-id="582b1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="582b1-122">-InputObject</span></span>
<span data-ttu-id="582b1-123">A representação de objeto do grupo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="582b1-123">The object representation of the group to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="582b1-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="582b1-124">-ObjectId</span></span>
<span data-ttu-id="582b1-125">A ID de objeto do grupo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="582b1-125">The object id of the group to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582b1-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="582b1-126">-PassThru</span></span>
<span data-ttu-id="582b1-127">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="582b1-127">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="582b1-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="582b1-128">-Confirm</span></span>
<span data-ttu-id="582b1-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="582b1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="582b1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="582b1-130">-WhatIf</span></span>
<span data-ttu-id="582b1-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="582b1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="582b1-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="582b1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="582b1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="582b1-133">CommonParameters</span></span>
<span data-ttu-id="582b1-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="582b1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="582b1-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="582b1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="582b1-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="582b1-136">INPUTS</span></span>

### <span data-ttu-id="582b1-137">System. String</span><span class="sxs-lookup"><span data-stu-id="582b1-137">System.String</span></span>

### <span data-ttu-id="582b1-138">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="582b1-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="582b1-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="582b1-139">OUTPUTS</span></span>

### <span data-ttu-id="582b1-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="582b1-140">System.Boolean</span></span>

## <span data-ttu-id="582b1-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="582b1-141">NOTES</span></span>

## <span data-ttu-id="582b1-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="582b1-142">RELATED LINKS</span></span>
