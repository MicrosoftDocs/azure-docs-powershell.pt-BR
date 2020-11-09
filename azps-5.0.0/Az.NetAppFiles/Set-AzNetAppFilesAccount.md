---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: ecbf6a847ad208b49e11ab0089f9cf486763ddf3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94282053"
---
# <span data-ttu-id="c2981-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="c2981-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="c2981-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c2981-102">SYNOPSIS</span></span>
<span data-ttu-id="c2981-103">Atualiza uma conta do Azure NetApp Files (ANF) com o novo conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="c2981-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="c2981-104">Útil para exclusão de diretórios ativos associados.</span><span class="sxs-lookup"><span data-stu-id="c2981-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="c2981-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2981-105">SYNTAX</span></span>

### <span data-ttu-id="c2981-106">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c2981-106">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2981-107">SetByResourceActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="c2981-107">SetByResourceActiveDirectory</span></span>
```
Set-AzNetAppFilesAccount -Location <String> -Name <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2981-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c2981-108">DESCRIPTION</span></span>
<span data-ttu-id="c2981-109">O cmdlet **set-AzNetAppFilesAccount** modifica uma conta ANF.</span><span class="sxs-lookup"><span data-stu-id="c2981-109">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="c2981-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c2981-110">EXAMPLES</span></span>

### <span data-ttu-id="c2981-111">Exemplo 1: modificar uma conta do ANF</span><span class="sxs-lookup"><span data-stu-id="c2981-111">Example 1 : Modify an ANF account</span></span>
```
PS C:\>Set-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="c2981-112">Esse comando executa uma atualização na conta fornecida.</span><span class="sxs-lookup"><span data-stu-id="c2981-112">This command performs an update on the given account.</span></span> <span data-ttu-id="c2981-113">A ausência do Active Directory significa que ela será removida da conta.</span><span class="sxs-lookup"><span data-stu-id="c2981-113">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="c2981-114">OS</span><span class="sxs-lookup"><span data-stu-id="c2981-114">PARAMETERS</span></span>

### <span data-ttu-id="c2981-115">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="c2981-115">-ActiveDirectory</span></span>
<span data-ttu-id="c2981-116">Uma matriz de Hashtable que representa os diretórios ativos</span><span class="sxs-lookup"><span data-stu-id="c2981-116">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: SetByResourceActiveDirectory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2981-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2981-117">-DefaultProfile</span></span>
<span data-ttu-id="c2981-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c2981-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2981-119">-Local</span><span class="sxs-lookup"><span data-stu-id="c2981-119">-Location</span></span>
<span data-ttu-id="c2981-120">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="c2981-120">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2981-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c2981-121">-Name</span></span>
<span data-ttu-id="c2981-122">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="c2981-122">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2981-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2981-123">-ResourceGroupName</span></span>
<span data-ttu-id="c2981-124">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="c2981-124">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="c2981-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="c2981-125">-Tag</span></span>
<span data-ttu-id="c2981-126">Uma Hashtable que representa as marcas de recursos</span><span class="sxs-lookup"><span data-stu-id="c2981-126">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2981-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c2981-127">-Confirm</span></span>
<span data-ttu-id="c2981-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2981-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2981-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2981-129">-WhatIf</span></span>
<span data-ttu-id="c2981-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c2981-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2981-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c2981-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2981-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2981-132">CommonParameters</span></span>
<span data-ttu-id="c2981-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2981-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2981-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2981-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2981-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c2981-135">INPUTS</span></span>

### <span data-ttu-id="c2981-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c2981-136">None</span></span>

## <span data-ttu-id="c2981-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c2981-137">OUTPUTS</span></span>

### <span data-ttu-id="c2981-138">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="c2981-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="c2981-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c2981-139">NOTES</span></span>

## <span data-ttu-id="c2981-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c2981-140">RELATED LINKS</span></span>
