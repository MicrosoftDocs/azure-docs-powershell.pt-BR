---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
ms.openlocfilehash: fdadfde6c798bf404d1f99dbb1ff2a8109d41f73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772136"
---
# <span data-ttu-id="ae044-101">New-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="ae044-101">New-AzNetAppFilesPool</span></span>

## <span data-ttu-id="ae044-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae044-102">SYNOPSIS</span></span>
<span data-ttu-id="ae044-103">Cria um novo pool de arquivos do Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="ae044-103">Creates a new Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="ae044-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae044-104">SYNTAX</span></span>

### <span data-ttu-id="ae044-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ae044-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae044-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae044-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String> [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae044-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae044-107">DESCRIPTION</span></span>
<span data-ttu-id="ae044-108">O cmdlet **New-AzNetAppFilesPool** cria um pool ANF.</span><span class="sxs-lookup"><span data-stu-id="ae044-108">The **New-AzNetAppFilesPool** cmdlet creates an ANF pool.</span></span>

## <span data-ttu-id="ae044-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae044-109">EXAMPLES</span></span>

### <span data-ttu-id="ae044-110">Exemplo 1: criar um pool de ANF</span><span class="sxs-lookup"><span data-stu-id="ae044-110">Example 1: Create an ANF pool</span></span>
```
PS C:\>New-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool" -l "westus2" -PoolSize 4398046511104 -ServiceLevel "Premium"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
ProvisioningState : Succeeded
```

<span data-ttu-id="ae044-111">Esse comando cria o novo pool de ANF "MyAnfPool" na conta "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="ae044-111">This command creates the new ANF pool "MyAnfPool" within the account "MyAnfAccount".</span></span>

## <span data-ttu-id="ae044-112">OS</span><span class="sxs-lookup"><span data-stu-id="ae044-112">PARAMETERS</span></span>

### <span data-ttu-id="ae044-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ae044-113">-AccountName</span></span>
<span data-ttu-id="ae044-114">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="ae044-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="ae044-115">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="ae044-115">-AccountObject</span></span>
<span data-ttu-id="ae044-116">A conta para o novo objeto de pool</span><span class="sxs-lookup"><span data-stu-id="ae044-116">The account for the new pool object</span></span>

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

### <span data-ttu-id="ae044-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae044-117">-DefaultProfile</span></span>
<span data-ttu-id="ae044-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae044-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae044-119">-Local</span><span class="sxs-lookup"><span data-stu-id="ae044-119">-Location</span></span>
<span data-ttu-id="ae044-120">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="ae044-120">The location of the resource</span></span>

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

### <span data-ttu-id="ae044-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae044-121">-Name</span></span>
<span data-ttu-id="ae044-122">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="ae044-122">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae044-123">-Agrupamento</span><span class="sxs-lookup"><span data-stu-id="ae044-123">-PoolSize</span></span>
<span data-ttu-id="ae044-124">O tamanho do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="ae044-124">The size of the ANF pool</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae044-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae044-125">-ResourceGroupName</span></span>
<span data-ttu-id="ae044-126">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="ae044-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="ae044-127">-Nível de</span><span class="sxs-lookup"><span data-stu-id="ae044-127">-ServiceLevel</span></span>
<span data-ttu-id="ae044-128">O nível de serviço do pool ANF</span><span class="sxs-lookup"><span data-stu-id="ae044-128">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="ae044-129">-Marca</span><span class="sxs-lookup"><span data-stu-id="ae044-129">-Tag</span></span>
<span data-ttu-id="ae044-130">Uma Hashtable que representa as marcas de recursos</span><span class="sxs-lookup"><span data-stu-id="ae044-130">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="ae044-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ae044-131">-Confirm</span></span>
<span data-ttu-id="ae044-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae044-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae044-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae044-133">-WhatIf</span></span>
<span data-ttu-id="ae044-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ae044-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae044-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae044-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae044-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae044-136">CommonParameters</span></span>
<span data-ttu-id="ae044-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae044-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ae044-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae044-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae044-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae044-139">INPUTS</span></span>

### <span data-ttu-id="ae044-140">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="ae044-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="ae044-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae044-141">OUTPUTS</span></span>

### <span data-ttu-id="ae044-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="ae044-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="ae044-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae044-143">NOTES</span></span>

## <span data-ttu-id="ae044-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae044-144">RELATED LINKS</span></span>