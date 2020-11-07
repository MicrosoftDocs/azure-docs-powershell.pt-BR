---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: e6fa7a00218e52eae6b0323bc5e8ac25459986ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777236"
---
# <span data-ttu-id="1dedb-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="1dedb-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="1dedb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1dedb-102">SYNOPSIS</span></span>
<span data-ttu-id="1dedb-103">Atualiza uma conta do Azure NetApp Files (ANF) de acordo com os modificadores opcionais fornecidos.</span><span class="sxs-lookup"><span data-stu-id="1dedb-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="1dedb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1dedb-104">SYNTAX</span></span>

```
Update-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-Location <String>]
 [-ActiveDirectories <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```
### <span data-ttu-id="1dedb-105">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dedb-105">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1dedb-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dedb-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dedb-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dedb-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1dedb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1dedb-108">DESCRIPTION</span></span>
<span data-ttu-id="1dedb-109">O cmdlet **Update-AzNetAppFilesAccount** modifica uma conta ANF.</span><span class="sxs-lookup"><span data-stu-id="1dedb-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="1dedb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1dedb-110">EXAMPLES</span></span>

### <span data-ttu-id="1dedb-111">Exemplo 1: atualiza uma conta do ANF</span><span class="sxs-lookup"><span data-stu-id="1dedb-111">Example 1 : Updates an ANF account</span></span>
```
PS C:\>Update-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount" -Tag @{'Tag1' = 'Value1'}

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              : {Tag1}
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories :
ProvisioningState : Succeeded
```

<span data-ttu-id="1dedb-112">Esse comando executa uma atualização na conta determinada modificando as marcas para as fornecidas.</span><span class="sxs-lookup"><span data-stu-id="1dedb-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="1dedb-113">OS</span><span class="sxs-lookup"><span data-stu-id="1dedb-113">PARAMETERS</span></span>

### <span data-ttu-id="1dedb-114">-ActiveDirectories</span><span class="sxs-lookup"><span data-stu-id="1dedb-114">-ActiveDirectories</span></span>
<span data-ttu-id="1dedb-115">Uma matriz de Hashtable que representa os diretórios ativos</span><span class="sxs-lookup"><span data-stu-id="1dedb-115">A hashtable array which represents the active directories</span></span>

```yaml
Type: PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dedb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dedb-116">-DefaultProfile</span></span>
<span data-ttu-id="1dedb-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1dedb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dedb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dedb-118">-InputObject</span></span>
<span data-ttu-id="1dedb-119">O objeto de conta a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="1dedb-119">The account object to update</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dedb-120">-Local</span><span class="sxs-lookup"><span data-stu-id="1dedb-120">-Location</span></span>
<span data-ttu-id="1dedb-121">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="1dedb-121">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dedb-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1dedb-122">-Name</span></span>
<span data-ttu-id="1dedb-123">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="1dedb-123">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dedb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dedb-124">-ResourceGroupName</span></span>
<span data-ttu-id="1dedb-125">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="1dedb-125">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dedb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1dedb-126">-ResourceId</span></span>
<span data-ttu-id="1dedb-127">A ID do recurso da conta ANF</span><span class="sxs-lookup"><span data-stu-id="1dedb-127">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="1dedb-128">-Marca</span><span class="sxs-lookup"><span data-stu-id="1dedb-128">-Tag</span></span>
<span data-ttu-id="1dedb-129">Uma Hashtable que representa as marcas de recursos</span><span class="sxs-lookup"><span data-stu-id="1dedb-129">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dedb-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1dedb-130">-Confirm</span></span>
<span data-ttu-id="1dedb-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dedb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dedb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dedb-132">-WhatIf</span></span>
<span data-ttu-id="1dedb-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1dedb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dedb-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1dedb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dedb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dedb-135">CommonParameters</span></span>
<span data-ttu-id="1dedb-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dedb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1dedb-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dedb-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dedb-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1dedb-138">INPUTS</span></span>

### <span data-ttu-id="1dedb-139">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1dedb-139">None</span></span>

## <span data-ttu-id="1dedb-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1dedb-140">OUTPUTS</span></span>

### <span data-ttu-id="1dedb-141">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="1dedb-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="1dedb-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1dedb-142">NOTES</span></span>

## <span data-ttu-id="1dedb-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1dedb-143">RELATED LINKS</span></span>
