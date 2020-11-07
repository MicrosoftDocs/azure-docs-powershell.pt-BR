---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: d2a379567ab96f5776b55c4cfbac2eabeaeb02a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777237"
---
# <span data-ttu-id="196f9-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="196f9-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="196f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="196f9-102">SYNOPSIS</span></span>
<span data-ttu-id="196f9-103">Atualiza uma conta do Azure NetApp Files (ANF) com o novo conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="196f9-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="196f9-104">Útil para exclusão de diretórios ativos associados.</span><span class="sxs-lookup"><span data-stu-id="196f9-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="196f9-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="196f9-105">SYNTAX</span></span>

```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectories <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="196f9-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="196f9-106">DESCRIPTION</span></span>
<span data-ttu-id="196f9-107">O cmdlet **set-AzNetAppFilesAccount** modifica uma conta ANF.</span><span class="sxs-lookup"><span data-stu-id="196f9-107">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="196f9-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="196f9-108">EXAMPLES</span></span>

### <span data-ttu-id="196f9-109">Exemplo 1: modificar uma conta do ANF</span><span class="sxs-lookup"><span data-stu-id="196f9-109">Example 1 : Modify an ANF account</span></span>
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

<span data-ttu-id="196f9-110">Esse comando executa uma atualização na conta fornecida.</span><span class="sxs-lookup"><span data-stu-id="196f9-110">This command performs an update on the given account.</span></span> <span data-ttu-id="196f9-111">A ausência do Active Directory significa que ela será removida da conta.</span><span class="sxs-lookup"><span data-stu-id="196f9-111">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="196f9-112">OS</span><span class="sxs-lookup"><span data-stu-id="196f9-112">PARAMETERS</span></span>

### <span data-ttu-id="196f9-113">-ActiveDirectories</span><span class="sxs-lookup"><span data-stu-id="196f9-113">-ActiveDirectories</span></span>
<span data-ttu-id="196f9-114">Uma matriz de Hashtable que representa os diretórios ativos</span><span class="sxs-lookup"><span data-stu-id="196f9-114">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="196f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="196f9-115">-DefaultProfile</span></span>
<span data-ttu-id="196f9-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="196f9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="196f9-117">-Local</span><span class="sxs-lookup"><span data-stu-id="196f9-117">-Location</span></span>
<span data-ttu-id="196f9-118">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="196f9-118">The location of the resource</span></span>

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

### <span data-ttu-id="196f9-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="196f9-119">-Name</span></span>
<span data-ttu-id="196f9-120">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="196f9-120">The name of the ANF account</span></span>

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

### <span data-ttu-id="196f9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="196f9-121">-ResourceGroupName</span></span>
<span data-ttu-id="196f9-122">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="196f9-122">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="196f9-123">-Marca</span><span class="sxs-lookup"><span data-stu-id="196f9-123">-Tag</span></span>
<span data-ttu-id="196f9-124">Uma Hashtable que representa as marcas de recursos</span><span class="sxs-lookup"><span data-stu-id="196f9-124">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="196f9-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="196f9-125">-Confirm</span></span>
<span data-ttu-id="196f9-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="196f9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="196f9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="196f9-127">-WhatIf</span></span>
<span data-ttu-id="196f9-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="196f9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="196f9-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="196f9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="196f9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="196f9-130">CommonParameters</span></span>
<span data-ttu-id="196f9-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="196f9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="196f9-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="196f9-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="196f9-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="196f9-133">INPUTS</span></span>

### <span data-ttu-id="196f9-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="196f9-134">None</span></span>

## <span data-ttu-id="196f9-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="196f9-135">OUTPUTS</span></span>

### <span data-ttu-id="196f9-136">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="196f9-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="196f9-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="196f9-137">NOTES</span></span>

## <span data-ttu-id="196f9-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="196f9-138">RELATED LINKS</span></span>
