---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: d41ce912761770d724fd700249f07d0af11c9647
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113535"
---
# <span data-ttu-id="8b784-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="8b784-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="8b784-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b784-102">SYNOPSIS</span></span>
<span data-ttu-id="8b784-103">Obtém detalhes de um pool de Arquivos do Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="8b784-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="8b784-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b784-104">SYNTAX</span></span>

### <span data-ttu-id="8b784-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8b784-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b784-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b784-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b784-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b784-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b784-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8b784-108">DESCRIPTION</span></span>
<span data-ttu-id="8b784-109">O cmdlet **Get-AzNetAppFilesPool** obtém detalhes de um pool ANF.</span><span class="sxs-lookup"><span data-stu-id="8b784-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="8b784-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8b784-110">EXAMPLES</span></span>

### <span data-ttu-id="8b784-111">Exemplo 1: Obter um pool de ANF</span><span class="sxs-lookup"><span data-stu-id="8b784-111">Example 1: Get an ANF pool</span></span>
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

<span data-ttu-id="8b784-112">Esse comando obtém a conta chamada MyAnfPool da conta "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="8b784-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="8b784-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b784-113">PARAMETERS</span></span>

### <span data-ttu-id="8b784-114">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="8b784-114">-AccountName</span></span>
<span data-ttu-id="8b784-115">O nome da conta da ANF</span><span class="sxs-lookup"><span data-stu-id="8b784-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="8b784-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="8b784-116">-AccountObject</span></span>
<span data-ttu-id="8b784-117">O objeto da conta que contém o pool a ser retornado</span><span class="sxs-lookup"><span data-stu-id="8b784-117">The account object containing the pool to return</span></span>

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

### <span data-ttu-id="8b784-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b784-118">-DefaultProfile</span></span>
<span data-ttu-id="8b784-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8b784-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b784-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b784-120">-Name</span></span>
<span data-ttu-id="8b784-121">O nome do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="8b784-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="8b784-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b784-122">-ResourceGroupName</span></span>
<span data-ttu-id="8b784-123">O grupo de recursos do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="8b784-123">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="8b784-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b784-124">-ResourceId</span></span>
<span data-ttu-id="8b784-125">A ID do recurso do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="8b784-125">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="8b784-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b784-126">CommonParameters</span></span>
<span data-ttu-id="8b784-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b784-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b784-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b784-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b784-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="8b784-129">INPUTS</span></span>

### <span data-ttu-id="8b784-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8b784-130">System.String</span></span>

### <span data-ttu-id="8b784-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="8b784-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="8b784-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="8b784-132">OUTPUTS</span></span>

### <span data-ttu-id="8b784-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="8b784-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="8b784-134">Notas</span><span class="sxs-lookup"><span data-stu-id="8b784-134">NOTES</span></span>

## <span data-ttu-id="8b784-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b784-135">RELATED LINKS</span></span>
