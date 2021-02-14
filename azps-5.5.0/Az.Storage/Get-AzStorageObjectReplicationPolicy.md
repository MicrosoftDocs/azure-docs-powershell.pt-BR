---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 6785eac6df5568f4b26e6de61ac0f4bfd8061259
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117047"
---
# <span data-ttu-id="eed5b-101">Get-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="eed5b-101">Get-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="eed5b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eed5b-102">SYNOPSIS</span></span>
<span data-ttu-id="eed5b-103">Obtém ou lista a política de replicação de objeto de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="eed5b-103">Gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="eed5b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eed5b-104">SYNTAX</span></span>

### <span data-ttu-id="eed5b-105">Nomeda Conta (Padrão)</span><span class="sxs-lookup"><span data-stu-id="eed5b-105">AccountName (Default)</span></span>
```
Get-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eed5b-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="eed5b-106">AccountObject</span></span>
```
Get-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eed5b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="eed5b-107">DESCRIPTION</span></span>
<span data-ttu-id="eed5b-108">O **cmdlet Get-AzStorageObjectReplicationPolicy** obtém ou lista a política de replicação de objeto de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="eed5b-108">The **Get-AzStorageObjectReplicationPolicy** cmdlet gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="eed5b-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="eed5b-109">EXAMPLES</span></span>

### <span data-ttu-id="eed5b-110">Exemplo 1: Obter uma política de replicação de objeto com ID de política específica e mostrar suas regras.</span><span class="sxs-lookup"><span data-stu-id="eed5b-110">Example 1: Get an object replication policy with specific policy Id and show its rules.</span></span>
```
PS C:\> $policy = Get-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" -PolicyId 56bfa11c-81ef-4f8d-b307-5e5386e16fba

PS C:\> $policy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]

PS C:\> $policy.Rules

RuleId                               SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------                               --------------- -------------------- ------------------- -----------------------
d3d39a01-8d92-40e5-849f-e56209ae5cf5 src1            dest1                {}                                         
2407de9a-3301-4656-858f-359d185565e0 src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="eed5b-111">Esse comando obtém uma política de replicação de objeto com ID de política específica e mostra suas regras.</span><span class="sxs-lookup"><span data-stu-id="eed5b-111">This command gets an object replication policy with specific policy Id and show its rules.</span></span>

### <span data-ttu-id="eed5b-112">Exemplo 2:Política de replicação de objeto de lista de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="eed5b-112">Example 2:List object replication policy from a Storage account</span></span>
```
PS C:\> $policies = Get-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" 

PS C:\> $policies

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysrcaccount1   mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]
myresourcegroup   mydestaccount      68434c7a-20d0-4282-b75c-43b5a243435e             mysrcaccount2   mydestaccount      [d3d39a01-8d92-40e5-849f-e56209ae5cf5,...]
```

<span data-ttu-id="eed5b-113">Esse comando lista a política de replicação de objeto de uma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="eed5b-113">This command lists object replication policy from a Storage account.</span></span>

## <span data-ttu-id="eed5b-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eed5b-114">PARAMETERS</span></span>

### <span data-ttu-id="eed5b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eed5b-115">-DefaultProfile</span></span>
<span data-ttu-id="eed5b-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eed5b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eed5b-117">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="eed5b-117">-PolicyId</span></span>
<span data-ttu-id="eed5b-118">ID da Política de Replicação de Objeto.</span><span class="sxs-lookup"><span data-stu-id="eed5b-118">Object Replication Policy Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eed5b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eed5b-119">-ResourceGroupName</span></span>
<span data-ttu-id="eed5b-120">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eed5b-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eed5b-121">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="eed5b-121">-StorageAccount</span></span>
<span data-ttu-id="eed5b-122">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="eed5b-122">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eed5b-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="eed5b-123">-StorageAccountName</span></span>
<span data-ttu-id="eed5b-124">Nome da Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="eed5b-124">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eed5b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eed5b-125">CommonParameters</span></span>
<span data-ttu-id="eed5b-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eed5b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eed5b-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eed5b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eed5b-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="eed5b-128">INPUTS</span></span>

### <span data-ttu-id="eed5b-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eed5b-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="eed5b-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="eed5b-130">OUTPUTS</span></span>

### <span data-ttu-id="eed5b-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="eed5b-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="eed5b-132">Notas</span><span class="sxs-lookup"><span data-stu-id="eed5b-132">NOTES</span></span>

## <span data-ttu-id="eed5b-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eed5b-133">RELATED LINKS</span></span>
