---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
ms.openlocfilehash: 1d6c99a44e2163f2d441dcacc87cf202f334f330
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775929"
---
# <span data-ttu-id="855fe-101">Remove-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="855fe-101">Remove-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="855fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="855fe-102">SYNOPSIS</span></span>
<span data-ttu-id="855fe-103">Remove um usuário em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="855fe-103">Removes a user on a device.</span></span>

## <span data-ttu-id="855fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="855fe-104">SYNTAX</span></span>

### <span data-ttu-id="855fe-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="855fe-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="855fe-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="855fe-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="855fe-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="855fe-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-InputObject] <PSDataBoxEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="855fe-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="855fe-108">DESCRIPTION</span></span>
<span data-ttu-id="855fe-109">O cmdlet **Remove-AzDataBoxEdgeUser** remove um usuário do dispositivo de borda da caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="855fe-109">The **Remove-AzDataBoxEdgeUser** cmdlet removes a user on the Data Box Edge device.</span></span> <span data-ttu-id="855fe-110">Só há suporte para a criação de usuários do tipo `Share` .</span><span class="sxs-lookup"><span data-stu-id="855fe-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="855fe-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="855fe-111">EXAMPLES</span></span>

### <span data-ttu-id="855fe-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="855fe-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="855fe-113">OS</span><span class="sxs-lookup"><span data-stu-id="855fe-113">PARAMETERS</span></span>

### <span data-ttu-id="855fe-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="855fe-114">-AsJob</span></span>
<span data-ttu-id="855fe-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="855fe-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="855fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="855fe-116">-DefaultProfile</span></span>
<span data-ttu-id="855fe-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="855fe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="855fe-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="855fe-118">-DeviceName</span></span>
<span data-ttu-id="855fe-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="855fe-119">Device Name</span></span>

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

### <span data-ttu-id="855fe-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="855fe-120">-InputObject</span></span>
<span data-ttu-id="855fe-121">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="855fe-121">Input Object</span></span>

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

### <span data-ttu-id="855fe-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="855fe-122">-Name</span></span>
<span data-ttu-id="855fe-123">Nome de usuário</span><span class="sxs-lookup"><span data-stu-id="855fe-123">Username</span></span>

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

### <span data-ttu-id="855fe-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="855fe-124">-PassThru</span></span>
<span data-ttu-id="855fe-125">Retorna verdadeiro se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="855fe-125">returns true if successful</span></span>

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

### <span data-ttu-id="855fe-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="855fe-126">-ResourceGroupName</span></span>
<span data-ttu-id="855fe-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="855fe-127">Resource Group Name</span></span>

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

### <span data-ttu-id="855fe-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="855fe-128">-ResourceId</span></span>
<span data-ttu-id="855fe-129">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="855fe-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="855fe-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="855fe-130">-Confirm</span></span>
<span data-ttu-id="855fe-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="855fe-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="855fe-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="855fe-132">-WhatIf</span></span>
<span data-ttu-id="855fe-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="855fe-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="855fe-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="855fe-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="855fe-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="855fe-135">CommonParameters</span></span>
<span data-ttu-id="855fe-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="855fe-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="855fe-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="855fe-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="855fe-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="855fe-138">INPUTS</span></span>

### <span data-ttu-id="855fe-139">System. String</span><span class="sxs-lookup"><span data-stu-id="855fe-139">System.String</span></span>

### <span data-ttu-id="855fe-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="855fe-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="855fe-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="855fe-141">OUTPUTS</span></span>

### <span data-ttu-id="855fe-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="855fe-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="855fe-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="855fe-143">NOTES</span></span>

## <span data-ttu-id="855fe-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="855fe-144">RELATED LINKS</span></span>