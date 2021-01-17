---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
ms.openlocfilehash: 895974f12c7472cb93679cb27ca895ca40757f53
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427228"
---
# <span data-ttu-id="db819-101">Remove-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="db819-101">Remove-AzADGroup</span></span>

## <span data-ttu-id="db819-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db819-102">SYNOPSIS</span></span>
<span data-ttu-id="db819-103">Exclui um grupo do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="db819-103">Deletes an active directory group.</span></span>

## <span data-ttu-id="db819-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db819-104">SYNTAX</span></span>

### <span data-ttu-id="db819-105">ObjectIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="db819-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADGroup -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db819-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="db819-106">DisplayNameParameterSet</span></span>
```
Remove-AzADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db819-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db819-107">InputObjectParameterSet</span></span>
```
Remove-AzADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db819-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="db819-108">DESCRIPTION</span></span>
<span data-ttu-id="db819-109">Exclui um grupo do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="db819-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="db819-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db819-110">EXAMPLES</span></span>

### <span data-ttu-id="db819-111">Exemplo 1: remover um grupo por ID de objeto</span><span class="sxs-lookup"><span data-stu-id="db819-111">Example 1: Remove a group by object id</span></span>

```powershell
PS C:\> Remove-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="db819-112">Remove o grupo com a ID de objeto "85F89C90-780E-4AA6-9F4F-6F268D322EEE" do locatário.</span><span class="sxs-lookup"><span data-stu-id="db819-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="db819-113">Exemplo 2: remover um grupo por tubulação</span><span class="sxs-lookup"><span data-stu-id="db819-113">Example 2: Remove a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroup
```

<span data-ttu-id="db819-114">Obtém o grupo com a ID de objeto ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' e canaliza-se para Remove-AzADGroup para remover o grupo do locatário.</span><span class="sxs-lookup"><span data-stu-id="db819-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="db819-115">OS</span><span class="sxs-lookup"><span data-stu-id="db819-115">PARAMETERS</span></span>

### <span data-ttu-id="db819-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db819-116">-DefaultProfile</span></span>
<span data-ttu-id="db819-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db819-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db819-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="db819-118">-DisplayName</span></span>
<span data-ttu-id="db819-119">O nome de exibição do grupo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="db819-119">The display name of the group to be removed.</span></span>

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

### <span data-ttu-id="db819-120">-Force</span><span class="sxs-lookup"><span data-stu-id="db819-120">-Force</span></span>
<span data-ttu-id="db819-121">Se especificado, não pede confirmação para excluir o grupo.</span><span class="sxs-lookup"><span data-stu-id="db819-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

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

### <span data-ttu-id="db819-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db819-122">-InputObject</span></span>
<span data-ttu-id="db819-123">A representação de objeto do grupo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="db819-123">The object representation of the group to be removed.</span></span>

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

### <span data-ttu-id="db819-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="db819-124">-ObjectId</span></span>
<span data-ttu-id="db819-125">A ID de objeto do grupo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="db819-125">The object id of the group to be removed.</span></span>

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

### <span data-ttu-id="db819-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db819-126">-PassThru</span></span>
<span data-ttu-id="db819-127">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="db819-127">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="db819-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="db819-128">-Confirm</span></span>
<span data-ttu-id="db819-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db819-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db819-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db819-130">-WhatIf</span></span>
<span data-ttu-id="db819-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="db819-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db819-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="db819-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db819-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db819-133">CommonParameters</span></span>
<span data-ttu-id="db819-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db819-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db819-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db819-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db819-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="db819-136">INPUTS</span></span>

### <span data-ttu-id="db819-137">System. String</span><span class="sxs-lookup"><span data-stu-id="db819-137">System.String</span></span>

### <span data-ttu-id="db819-138">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="db819-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="db819-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="db819-139">OUTPUTS</span></span>

### <span data-ttu-id="db819-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="db819-140">System.Boolean</span></span>

## <span data-ttu-id="db819-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="db819-141">NOTES</span></span>

## <span data-ttu-id="db819-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db819-142">RELATED LINKS</span></span>