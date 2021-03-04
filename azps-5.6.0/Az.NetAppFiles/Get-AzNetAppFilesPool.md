---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: 546364e96f7beed16ae8786dc3aaacbf9a84454d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887463"
---
# <span data-ttu-id="47901-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="47901-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="47901-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47901-102">SYNOPSIS</span></span>
<span data-ttu-id="47901-103">Obtém detalhes de um pool de Arquivos do Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="47901-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="47901-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="47901-104">SYNTAX</span></span>

### <span data-ttu-id="47901-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="47901-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47901-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47901-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47901-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47901-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="47901-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="47901-108">DESCRIPTION</span></span>
<span data-ttu-id="47901-109">O cmdlet **Get-AzNetAppFilesPool** obtém detalhes de um pool ANF.</span><span class="sxs-lookup"><span data-stu-id="47901-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="47901-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47901-110">EXAMPLES</span></span>

### <span data-ttu-id="47901-111">Exemplo 1: Obter um pool ANF</span><span class="sxs-lookup"><span data-stu-id="47901-111">Example 1: Get an ANF pool</span></span>
```
PS C:\>Get-AzAnfPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
TotalThroughputMibps: 262.144
UtilizedThroughputMibps: 164.221
QosType           : Auto
ProvisioningState : Succeeded
```

<span data-ttu-id="47901-112">Este comando obtém a conta chamada MyAnfPool da conta "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="47901-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="47901-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="47901-113">PARAMETERS</span></span>

### <span data-ttu-id="47901-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="47901-114">-AccountName</span></span>
<span data-ttu-id="47901-115">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="47901-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="47901-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="47901-116">-AccountObject</span></span>
<span data-ttu-id="47901-117">O objeto account que contém o pool a ser retornado</span><span class="sxs-lookup"><span data-stu-id="47901-117">The account object containing the pool to return</span></span>

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

### <span data-ttu-id="47901-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47901-118">-DefaultProfile</span></span>
<span data-ttu-id="47901-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47901-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47901-120">-Name</span><span class="sxs-lookup"><span data-stu-id="47901-120">-Name</span></span>
<span data-ttu-id="47901-121">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="47901-121">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: PoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47901-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47901-122">-ResourceGroupName</span></span>
<span data-ttu-id="47901-123">O grupo de recursos do pool ANF</span><span class="sxs-lookup"><span data-stu-id="47901-123">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="47901-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47901-124">-ResourceId</span></span>
<span data-ttu-id="47901-125">A id de recurso do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="47901-125">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="47901-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47901-126">CommonParameters</span></span>
<span data-ttu-id="47901-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47901-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47901-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47901-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47901-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47901-129">INPUTS</span></span>

### <span data-ttu-id="47901-130">System.String</span><span class="sxs-lookup"><span data-stu-id="47901-130">System.String</span></span>

### <span data-ttu-id="47901-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="47901-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="47901-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="47901-132">OUTPUTS</span></span>

### <span data-ttu-id="47901-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="47901-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="47901-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="47901-134">NOTES</span></span>

## <span data-ttu-id="47901-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47901-135">RELATED LINKS</span></span>
