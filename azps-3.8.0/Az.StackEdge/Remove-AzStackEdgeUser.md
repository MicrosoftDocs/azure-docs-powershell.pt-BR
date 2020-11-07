---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
ms.openlocfilehash: ec8703b5b107758a331407d431f871acf249885d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943903"
---
# <span data-ttu-id="f7db8-101">Remove-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="f7db8-101">Remove-AzStackEdgeUser</span></span>

## <span data-ttu-id="f7db8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f7db8-102">SYNOPSIS</span></span>
<span data-ttu-id="f7db8-103">Remove um usuário em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f7db8-103">Removes a user on a device.</span></span>

## <span data-ttu-id="f7db8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7db8-104">SYNTAX</span></span>

### <span data-ttu-id="f7db8-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f7db8-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7db8-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7db8-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7db8-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7db8-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeUser [-InputObject] <PSStackEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7db8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f7db8-108">DESCRIPTION</span></span>
<span data-ttu-id="f7db8-109">O cmdlet **Remove-AzStackEdgeUser** remove um usuário no dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="f7db8-109">The **Remove-AzStackEdgeUser** cmdlet removes a user on the Stack Edge device.</span></span> <span data-ttu-id="f7db8-110">Só há suporte para a criação de usuários do tipo `Share` .</span><span class="sxs-lookup"><span data-stu-id="f7db8-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="f7db8-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7db8-111">EXAMPLES</span></span>

### <span data-ttu-id="f7db8-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f7db8-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="f7db8-113">OS</span><span class="sxs-lookup"><span data-stu-id="f7db8-113">PARAMETERS</span></span>

### <span data-ttu-id="f7db8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7db8-114">-AsJob</span></span>
<span data-ttu-id="f7db8-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f7db8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7db8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7db8-116">-DefaultProfile</span></span>
<span data-ttu-id="f7db8-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f7db8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7db8-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f7db8-118">-DeviceName</span></span>
<span data-ttu-id="f7db8-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="f7db8-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7db8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7db8-120">-InputObject</span></span>
<span data-ttu-id="f7db8-121">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="f7db8-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: User

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7db8-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7db8-122">-Name</span></span>
<span data-ttu-id="f7db8-123">Nome de usuário</span><span class="sxs-lookup"><span data-stu-id="f7db8-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7db8-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7db8-124">-PassThru</span></span>
<span data-ttu-id="f7db8-125">Retorna verdadeiro se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="f7db8-125">returns true if successful</span></span>

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

### <span data-ttu-id="f7db8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7db8-126">-ResourceGroupName</span></span>
<span data-ttu-id="f7db8-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f7db8-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7db8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7db8-128">-ResourceId</span></span>
<span data-ttu-id="f7db8-129">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="f7db8-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7db8-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f7db8-130">-Confirm</span></span>
<span data-ttu-id="f7db8-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7db8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7db8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7db8-132">-WhatIf</span></span>
<span data-ttu-id="f7db8-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f7db8-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7db8-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f7db8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7db8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7db8-135">CommonParameters</span></span>
<span data-ttu-id="f7db8-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7db8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7db8-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7db8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7db8-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f7db8-138">INPUTS</span></span>

### <span data-ttu-id="f7db8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f7db8-139">System.String</span></span>

### <span data-ttu-id="f7db8-140">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="f7db8-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="f7db8-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f7db8-141">OUTPUTS</span></span>

### <span data-ttu-id="f7db8-142">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="f7db8-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="f7db8-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f7db8-143">NOTES</span></span>

## <span data-ttu-id="f7db8-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7db8-144">RELATED LINKS</span></span>
