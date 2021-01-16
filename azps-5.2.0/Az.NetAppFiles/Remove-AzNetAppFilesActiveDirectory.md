---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 7fcf1f749816872fb7407fedaea10d06f3385441
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262605"
---
# <span data-ttu-id="8540c-101">Remove-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="8540c-101">Remove-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="8540c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8540c-102">SYNOPSIS</span></span>
<span data-ttu-id="8540c-103">Exclui uma configuração do Active Directory dos arquivos do Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="8540c-103">Deletes an Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="8540c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8540c-104">SYNTAX</span></span>

### <span data-ttu-id="8540c-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8540c-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8540c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8540c-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> -AccountObject <PSNetAppFilesAccount>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8540c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8540c-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -InputObject <PSNetAppFilesActiveDirectory> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8540c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8540c-108">DESCRIPTION</span></span>
<span data-ttu-id="8540c-109">O cmdlet **Remove-AzNetAppFilesActiveDirectory** exclui uma configuração do Active Directory do ANF.</span><span class="sxs-lookup"><span data-stu-id="8540c-109">The **Remove-AzNetAppFilesActiveDirectory** cmdlet deletes an ANF active directory configuration.</span></span>

## <span data-ttu-id="8540c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8540c-110">EXAMPLES</span></span>

### <span data-ttu-id="8540c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8540c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName"
```

<span data-ttu-id="8540c-112">Esse comando exclui a nova configuração do Active Directory do ANF com o nome "MyADName".</span><span class="sxs-lookup"><span data-stu-id="8540c-112">This command deletes the new ANF active directory configuration with a the name "MyADName".</span></span>

## <span data-ttu-id="8540c-113">OS</span><span class="sxs-lookup"><span data-stu-id="8540c-113">PARAMETERS</span></span>

### <span data-ttu-id="8540c-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8540c-114">-AccountName</span></span>
<span data-ttu-id="8540c-115">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="8540c-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="8540c-116">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="8540c-116">-AccountObject</span></span>
<span data-ttu-id="8540c-117">A conta para o objeto do Active Directory</span><span class="sxs-lookup"><span data-stu-id="8540c-117">The Account for the Active Directory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8540c-118">-ActiveDirectoryid</span><span class="sxs-lookup"><span data-stu-id="8540c-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="8540c-119">A ID do Active Directory do ANF</span><span class="sxs-lookup"><span data-stu-id="8540c-119">The ID of the ANF active directory</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8540c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8540c-120">-DefaultProfile</span></span>
<span data-ttu-id="8540c-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8540c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8540c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8540c-122">-InputObject</span></span>
<span data-ttu-id="8540c-123">O objeto do Active Directory a ser removido</span><span class="sxs-lookup"><span data-stu-id="8540c-123">The active directory object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8540c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8540c-124">-PassThru</span></span>
<span data-ttu-id="8540c-125">Retornar se o Active Directory especificado foi removido com êxito</span><span class="sxs-lookup"><span data-stu-id="8540c-125">Return whether the specified Active Directory  was successfully removed</span></span>

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

### <span data-ttu-id="8540c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8540c-126">-ResourceGroupName</span></span>
<span data-ttu-id="8540c-127">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="8540c-127">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="8540c-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8540c-128">-Confirm</span></span>
<span data-ttu-id="8540c-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8540c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8540c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8540c-130">-WhatIf</span></span>
<span data-ttu-id="8540c-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8540c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8540c-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8540c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8540c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8540c-133">CommonParameters</span></span>
<span data-ttu-id="8540c-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8540c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8540c-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8540c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8540c-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8540c-136">INPUTS</span></span>

### <span data-ttu-id="8540c-137">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="8540c-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="8540c-138">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="8540c-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="8540c-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8540c-139">OUTPUTS</span></span>

### <span data-ttu-id="8540c-140">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="8540c-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="8540c-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8540c-141">NOTES</span></span>

## <span data-ttu-id="8540c-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8540c-142">RELATED LINKS</span></span>
