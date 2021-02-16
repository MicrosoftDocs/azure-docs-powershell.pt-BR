---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: 9400efa61a98b6eb80b975d4999e03eb872e3b28
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113534"
---
# <span data-ttu-id="01e37-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="01e37-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="01e37-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="01e37-102">SYNOPSIS</span></span>
<span data-ttu-id="01e37-103">Exclui um volume de Arquivos Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="01e37-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="01e37-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01e37-104">SYNTAX</span></span>

### <span data-ttu-id="01e37-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="01e37-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01e37-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01e37-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01e37-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01e37-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01e37-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01e37-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01e37-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="01e37-109">DESCRIPTION</span></span>
<span data-ttu-id="01e37-110">O **cmdlet Remove-AzNetAppFilesVolume** exclui um volume ANF.</span><span class="sxs-lookup"><span data-stu-id="01e37-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="01e37-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="01e37-111">EXAMPLES</span></span>

### <span data-ttu-id="01e37-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="01e37-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="01e37-113">Esse comando exclui o volume da ANF "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="01e37-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="01e37-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01e37-114">PARAMETERS</span></span>

### <span data-ttu-id="01e37-115">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="01e37-115">-AccountName</span></span>
<span data-ttu-id="01e37-116">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="01e37-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01e37-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01e37-117">-DefaultProfile</span></span>
<span data-ttu-id="01e37-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="01e37-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01e37-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01e37-119">-InputObject</span></span>
<span data-ttu-id="01e37-120">O objeto de volume a ser removido</span><span class="sxs-lookup"><span data-stu-id="01e37-120">The volume object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01e37-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="01e37-121">-Name</span></span>
<span data-ttu-id="01e37-122">O nome do volume da ANF</span><span class="sxs-lookup"><span data-stu-id="01e37-122">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01e37-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01e37-123">-PassThru</span></span>
<span data-ttu-id="01e37-124">Retornar se o volume especificado foi removido com êxito</span><span class="sxs-lookup"><span data-stu-id="01e37-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="01e37-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="01e37-125">-PoolName</span></span>
<span data-ttu-id="01e37-126">O nome do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="01e37-126">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01e37-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="01e37-127">-PoolObject</span></span>
<span data-ttu-id="01e37-128">O objeto de pool que contém o volume a ser removido</span><span class="sxs-lookup"><span data-stu-id="01e37-128">The pool object containing the volume to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01e37-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01e37-129">-ResourceGroupName</span></span>
<span data-ttu-id="01e37-130">O grupo de recursos do volume de ANF</span><span class="sxs-lookup"><span data-stu-id="01e37-130">The resource group of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01e37-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01e37-131">-ResourceId</span></span>
<span data-ttu-id="01e37-132">A ID do recurso do volume da ANF</span><span class="sxs-lookup"><span data-stu-id="01e37-132">The resource id of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01e37-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="01e37-133">-Confirm</span></span>
<span data-ttu-id="01e37-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01e37-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01e37-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01e37-135">-WhatIf</span></span>
<span data-ttu-id="01e37-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="01e37-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01e37-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="01e37-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01e37-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01e37-138">CommonParameters</span></span>
<span data-ttu-id="01e37-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01e37-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01e37-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01e37-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01e37-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="01e37-141">INPUTS</span></span>

### <span data-ttu-id="01e37-142">System.String</span><span class="sxs-lookup"><span data-stu-id="01e37-142">System.String</span></span>

### <span data-ttu-id="01e37-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="01e37-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="01e37-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="01e37-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="01e37-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="01e37-145">OUTPUTS</span></span>

### <span data-ttu-id="01e37-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="01e37-146">System.Boolean</span></span>

## <span data-ttu-id="01e37-147">Notas</span><span class="sxs-lookup"><span data-stu-id="01e37-147">NOTES</span></span>

## <span data-ttu-id="01e37-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01e37-148">RELATED LINKS</span></span>
