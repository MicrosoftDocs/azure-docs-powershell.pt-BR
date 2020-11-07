---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: ef896185b606e107bb62208255a255655814fcbc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771855"
---
# <span data-ttu-id="b0382-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="b0382-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="b0382-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0382-102">SYNOPSIS</span></span>
<span data-ttu-id="b0382-103">Exclui um pool de arquivos do Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="b0382-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="b0382-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0382-104">SYNTAX</span></span>

### <span data-ttu-id="b0382-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b0382-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0382-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0382-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0382-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0382-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0382-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0382-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0382-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b0382-109">DESCRIPTION</span></span>
<span data-ttu-id="b0382-110">O cmdlet **Remove-AzNetAppFilesPool** exclui um pool ANF.</span><span class="sxs-lookup"><span data-stu-id="b0382-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="b0382-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0382-111">EXAMPLES</span></span>

### <span data-ttu-id="b0382-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b0382-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="b0382-113">Esse comando exclui o pool de ANF "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="b0382-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="b0382-114">OS</span><span class="sxs-lookup"><span data-stu-id="b0382-114">PARAMETERS</span></span>

### <span data-ttu-id="b0382-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b0382-115">-AccountName</span></span>
<span data-ttu-id="b0382-116">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="b0382-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="b0382-117">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="b0382-117">-AccountObject</span></span>
<span data-ttu-id="b0382-118">O objeto de conta que contém o pool a ser removido</span><span class="sxs-lookup"><span data-stu-id="b0382-118">The account object containing the pool to remove</span></span>

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

### <span data-ttu-id="b0382-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0382-119">-DefaultProfile</span></span>
<span data-ttu-id="b0382-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b0382-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0382-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0382-121">-InputObject</span></span>
<span data-ttu-id="b0382-122">O objeto de pool a ser removido</span><span class="sxs-lookup"><span data-stu-id="b0382-122">The pool object to remove</span></span>

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

### <span data-ttu-id="b0382-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0382-123">-Name</span></span>
<span data-ttu-id="b0382-124">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="b0382-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="b0382-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0382-125">-PassThru</span></span>
<span data-ttu-id="b0382-126">Retorna se o pool especificado foi removido com êxito</span><span class="sxs-lookup"><span data-stu-id="b0382-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="b0382-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0382-127">-ResourceGroupName</span></span>
<span data-ttu-id="b0382-128">O grupo de recursos do pool ANF</span><span class="sxs-lookup"><span data-stu-id="b0382-128">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="b0382-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0382-129">-ResourceId</span></span>
<span data-ttu-id="b0382-130">A ID do recurso do pool ANF</span><span class="sxs-lookup"><span data-stu-id="b0382-130">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="b0382-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b0382-131">-Confirm</span></span>
<span data-ttu-id="b0382-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0382-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0382-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0382-133">-WhatIf</span></span>
<span data-ttu-id="b0382-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b0382-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0382-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b0382-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0382-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0382-136">CommonParameters</span></span>
<span data-ttu-id="b0382-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0382-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b0382-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0382-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0382-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b0382-139">INPUTS</span></span>

### <span data-ttu-id="b0382-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b0382-140">System.String</span></span>

### <span data-ttu-id="b0382-141">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="b0382-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="b0382-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="b0382-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="b0382-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b0382-143">OUTPUTS</span></span>

### <span data-ttu-id="b0382-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b0382-144">System.Boolean</span></span>

## <span data-ttu-id="b0382-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b0382-145">NOTES</span></span>

## <span data-ttu-id="b0382-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0382-146">RELATED LINKS</span></span>
