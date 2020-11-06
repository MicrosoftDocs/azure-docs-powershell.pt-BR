---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: f6b21f3496f8ac05147db24de1df2ee03693fb7d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600762"
---
# <span data-ttu-id="922be-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="922be-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="922be-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="922be-102">SYNOPSIS</span></span>
<span data-ttu-id="922be-103">Exclui um volume de arquivos do Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="922be-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="922be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="922be-104">SYNTAX</span></span>

### <span data-ttu-id="922be-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="922be-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="922be-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="922be-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="922be-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="922be-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="922be-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="922be-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="922be-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="922be-109">DESCRIPTION</span></span>
<span data-ttu-id="922be-110">O cmdlet **Remove-AzNetAppFilesVolume** exclui um volume ANF.</span><span class="sxs-lookup"><span data-stu-id="922be-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="922be-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="922be-111">EXAMPLES</span></span>

### <span data-ttu-id="922be-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="922be-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="922be-113">Esse comando exclui o volume ANF "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="922be-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="922be-114">OS</span><span class="sxs-lookup"><span data-stu-id="922be-114">PARAMETERS</span></span>

### <span data-ttu-id="922be-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="922be-115">-AccountName</span></span>
<span data-ttu-id="922be-116">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="922be-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="922be-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="922be-117">-DefaultProfile</span></span>
<span data-ttu-id="922be-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="922be-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="922be-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="922be-119">-InputObject</span></span>
<span data-ttu-id="922be-120">O objeto volume a ser removido</span><span class="sxs-lookup"><span data-stu-id="922be-120">The volume object to remove</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="922be-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="922be-121">-Name</span></span>
<span data-ttu-id="922be-122">O nome do volume ANF</span><span class="sxs-lookup"><span data-stu-id="922be-122">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="922be-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="922be-123">-PassThru</span></span>
<span data-ttu-id="922be-124">Retornar se o volume especificado foi removido com êxito</span><span class="sxs-lookup"><span data-stu-id="922be-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="922be-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="922be-125">-PoolName</span></span>
<span data-ttu-id="922be-126">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="922be-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="922be-127">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="922be-127">-PoolObject</span></span>
<span data-ttu-id="922be-128">O objeto de pool que contém o volume a ser removido</span><span class="sxs-lookup"><span data-stu-id="922be-128">The pool object containing the volume to remove</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="922be-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="922be-129">-ResourceGroupName</span></span>
<span data-ttu-id="922be-130">O grupo de recursos do volume ANF</span><span class="sxs-lookup"><span data-stu-id="922be-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="922be-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="922be-131">-ResourceId</span></span>
<span data-ttu-id="922be-132">A ID do recurso do volume ANF</span><span class="sxs-lookup"><span data-stu-id="922be-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="922be-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="922be-133">-Confirm</span></span>
<span data-ttu-id="922be-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="922be-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="922be-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="922be-135">-WhatIf</span></span>
<span data-ttu-id="922be-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="922be-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="922be-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="922be-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="922be-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="922be-138">CommonParameters</span></span>
<span data-ttu-id="922be-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="922be-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="922be-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="922be-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="922be-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="922be-141">INPUTS</span></span>

### <span data-ttu-id="922be-142">System. String</span><span class="sxs-lookup"><span data-stu-id="922be-142">System.String</span></span>

### <span data-ttu-id="922be-143">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="922be-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="922be-144">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="922be-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="922be-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="922be-145">OUTPUTS</span></span>

### <span data-ttu-id="922be-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="922be-146">System.Boolean</span></span>

## <span data-ttu-id="922be-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="922be-147">NOTES</span></span>

## <span data-ttu-id="922be-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="922be-148">RELATED LINKS</span></span>
