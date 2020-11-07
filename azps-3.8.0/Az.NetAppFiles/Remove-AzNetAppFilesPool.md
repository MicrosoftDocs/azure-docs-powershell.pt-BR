---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: 717c1cac6def6fb51f1ab8b598f15a05a7d62db4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777239"
---
# <span data-ttu-id="6c8c1-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="6c8c1-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="6c8c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6c8c1-102">SYNOPSIS</span></span>
<span data-ttu-id="6c8c1-103">Exclui um pool de arquivos do Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="6c8c1-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="6c8c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6c8c1-104">SYNTAX</span></span>

### <span data-ttu-id="6c8c1-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6c8c1-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c8c1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c8c1-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c8c1-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c8c1-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c8c1-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c8c1-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c8c1-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6c8c1-109">DESCRIPTION</span></span>
<span data-ttu-id="6c8c1-110">O cmdlet **Remove-AzNetAppFilesPool** exclui um pool ANF.</span><span class="sxs-lookup"><span data-stu-id="6c8c1-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="6c8c1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6c8c1-111">EXAMPLES</span></span>

### <span data-ttu-id="6c8c1-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6c8c1-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="6c8c1-113">Esse comando exclui o pool de ANF "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="6c8c1-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="6c8c1-114">OS</span><span class="sxs-lookup"><span data-stu-id="6c8c1-114">PARAMETERS</span></span>

### <span data-ttu-id="6c8c1-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6c8c1-115">-AccountName</span></span>
<span data-ttu-id="6c8c1-116">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="6c8c1-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c8c1-117">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="6c8c1-117">-AccountObject</span></span>
<span data-ttu-id="6c8c1-118">O objeto de conta que contém o pool a ser removido</span><span class="sxs-lookup"><span data-stu-id="6c8c1-118">The account object containing the pool to remove</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c8c1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c8c1-119">-DefaultProfile</span></span>
<span data-ttu-id="6c8c1-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6c8c1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c8c1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c8c1-121">-InputObject</span></span>
<span data-ttu-id="6c8c1-122">O objeto de pool a ser removido</span><span class="sxs-lookup"><span data-stu-id="6c8c1-122">The pool object to remove</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c8c1-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c8c1-123">-Name</span></span>
<span data-ttu-id="6c8c1-124">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="6c8c1-124">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c8c1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c8c1-125">-PassThru</span></span>
<span data-ttu-id="6c8c1-126">Retorna se o pool especificado foi removido com êxito</span><span class="sxs-lookup"><span data-stu-id="6c8c1-126">Return whether the specified pool was successfully removed</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c8c1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c8c1-127">-ResourceGroupName</span></span>
<span data-ttu-id="6c8c1-128">O grupo de recursos do pool ANF</span><span class="sxs-lookup"><span data-stu-id="6c8c1-128">The resource group of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c8c1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c8c1-129">-ResourceId</span></span>
<span data-ttu-id="6c8c1-130">A ID do recurso do pool ANF</span><span class="sxs-lookup"><span data-stu-id="6c8c1-130">The resource id of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c8c1-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6c8c1-131">-Confirm</span></span>
<span data-ttu-id="6c8c1-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c8c1-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c8c1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c8c1-133">-WhatIf</span></span>
<span data-ttu-id="6c8c1-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6c8c1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c8c1-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6c8c1-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c8c1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c8c1-136">CommonParameters</span></span>
<span data-ttu-id="6c8c1-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c8c1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6c8c1-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c8c1-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c8c1-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6c8c1-139">INPUTS</span></span>

### <span data-ttu-id="6c8c1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6c8c1-140">System.String</span></span>

### <span data-ttu-id="6c8c1-141">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="6c8c1-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="6c8c1-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="6c8c1-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="6c8c1-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6c8c1-143">OUTPUTS</span></span>

### <span data-ttu-id="6c8c1-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6c8c1-144">System.Boolean</span></span>

## <span data-ttu-id="6c8c1-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6c8c1-145">NOTES</span></span>

## <span data-ttu-id="6c8c1-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6c8c1-146">RELATED LINKS</span></span>
