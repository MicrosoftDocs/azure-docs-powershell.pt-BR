---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
ms.openlocfilehash: cecfa3e009f6d6fbc7167c4b8f1ca110d547b5b7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127040"
---
# <span data-ttu-id="cfd6a-101">Remove-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="cfd6a-101">Remove-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="cfd6a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cfd6a-102">SYNOPSIS</span></span>
<span data-ttu-id="cfd6a-103">Remove um usuário em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cfd6a-103">Removes a user on a device.</span></span>

## <span data-ttu-id="cfd6a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cfd6a-104">SYNTAX</span></span>

### <span data-ttu-id="cfd6a-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cfd6a-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfd6a-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfd6a-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfd6a-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfd6a-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-InputObject] <PSDataBoxEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfd6a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="cfd6a-108">DESCRIPTION</span></span>
<span data-ttu-id="cfd6a-109">O cmdlet **Remove-AzDataBoxEdgeUser** remove um usuário no dispositivo de Borda da Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="cfd6a-109">The **Remove-AzDataBoxEdgeUser** cmdlet removes a user on the Data Box Edge device.</span></span> <span data-ttu-id="cfd6a-110">Há suporte para a criação de apenas usuários `Share` do tipo.</span><span class="sxs-lookup"><span data-stu-id="cfd6a-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="cfd6a-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cfd6a-111">EXAMPLES</span></span>

### <span data-ttu-id="cfd6a-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cfd6a-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="cfd6a-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cfd6a-113">PARAMETERS</span></span>

### <span data-ttu-id="cfd6a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cfd6a-114">-AsJob</span></span>
<span data-ttu-id="cfd6a-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cfd6a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cfd6a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfd6a-116">-DefaultProfile</span></span>
<span data-ttu-id="cfd6a-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cfd6a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfd6a-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="cfd6a-118">-DeviceName</span></span>
<span data-ttu-id="cfd6a-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="cfd6a-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfd6a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cfd6a-120">-InputObject</span></span>
<span data-ttu-id="cfd6a-121">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="cfd6a-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfd6a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="cfd6a-122">-Name</span></span>
<span data-ttu-id="cfd6a-123">Username</span><span class="sxs-lookup"><span data-stu-id="cfd6a-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfd6a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cfd6a-124">-PassThru</span></span>
<span data-ttu-id="cfd6a-125">retorna verdadeiro se for bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="cfd6a-125">returns true if successful</span></span>

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

### <span data-ttu-id="cfd6a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfd6a-126">-ResourceGroupName</span></span>
<span data-ttu-id="cfd6a-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="cfd6a-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfd6a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfd6a-128">-ResourceId</span></span>
<span data-ttu-id="cfd6a-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfd6a-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="cfd6a-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="cfd6a-130">-Confirm</span></span>
<span data-ttu-id="cfd6a-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfd6a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfd6a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfd6a-132">-WhatIf</span></span>
<span data-ttu-id="cfd6a-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="cfd6a-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cfd6a-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cfd6a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfd6a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfd6a-135">CommonParameters</span></span>
<span data-ttu-id="cfd6a-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfd6a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfd6a-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cfd6a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfd6a-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="cfd6a-138">INPUTS</span></span>

### <span data-ttu-id="cfd6a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="cfd6a-139">System.String</span></span>

### <span data-ttu-id="cfd6a-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="cfd6a-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="cfd6a-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="cfd6a-141">OUTPUTS</span></span>

### <span data-ttu-id="cfd6a-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="cfd6a-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="cfd6a-143">Notas</span><span class="sxs-lookup"><span data-stu-id="cfd6a-143">NOTES</span></span>

## <span data-ttu-id="cfd6a-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cfd6a-144">RELATED LINKS</span></span>
