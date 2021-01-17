---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: d41ce912761770d724fd700249f07d0af11c9647
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427073"
---
# <span data-ttu-id="0617e-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="0617e-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="0617e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0617e-102">SYNOPSIS</span></span>
<span data-ttu-id="0617e-103">Obtém detalhes de um pool de arquivos do Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="0617e-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="0617e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0617e-104">SYNTAX</span></span>

### <span data-ttu-id="0617e-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0617e-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0617e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0617e-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0617e-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0617e-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0617e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0617e-108">DESCRIPTION</span></span>
<span data-ttu-id="0617e-109">O cmdlet **Get-AzNetAppFilesPool** Obtém detalhes de um pool de ANF.</span><span class="sxs-lookup"><span data-stu-id="0617e-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="0617e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0617e-110">EXAMPLES</span></span>

### <span data-ttu-id="0617e-111">Exemplo 1: obter um pool ANF</span><span class="sxs-lookup"><span data-stu-id="0617e-111">Example 1: Get an ANF pool</span></span>
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

<span data-ttu-id="0617e-112">Esse comando obtém a conta chamada MyAnfPool da conta "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="0617e-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="0617e-113">OS</span><span class="sxs-lookup"><span data-stu-id="0617e-113">PARAMETERS</span></span>

### <span data-ttu-id="0617e-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0617e-114">-AccountName</span></span>
<span data-ttu-id="0617e-115">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="0617e-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="0617e-116">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="0617e-116">-AccountObject</span></span>
<span data-ttu-id="0617e-117">O objeto de conta que contém o pool a ser retornado</span><span class="sxs-lookup"><span data-stu-id="0617e-117">The account object containing the pool to return</span></span>

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

### <span data-ttu-id="0617e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0617e-118">-DefaultProfile</span></span>
<span data-ttu-id="0617e-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0617e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0617e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="0617e-120">-Name</span></span>
<span data-ttu-id="0617e-121">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="0617e-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="0617e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0617e-122">-ResourceGroupName</span></span>
<span data-ttu-id="0617e-123">O grupo de recursos do pool ANF</span><span class="sxs-lookup"><span data-stu-id="0617e-123">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="0617e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0617e-124">-ResourceId</span></span>
<span data-ttu-id="0617e-125">A ID do recurso do pool ANF</span><span class="sxs-lookup"><span data-stu-id="0617e-125">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="0617e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0617e-126">CommonParameters</span></span>
<span data-ttu-id="0617e-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0617e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0617e-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0617e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0617e-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0617e-129">INPUTS</span></span>

### <span data-ttu-id="0617e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0617e-130">System.String</span></span>

### <span data-ttu-id="0617e-131">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="0617e-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="0617e-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0617e-132">OUTPUTS</span></span>

### <span data-ttu-id="0617e-133">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="0617e-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="0617e-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0617e-134">NOTES</span></span>

## <span data-ttu-id="0617e-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0617e-135">RELATED LINKS</span></span>
