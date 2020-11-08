---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 6785eac6df5568f4b26e6de61ac0f4bfd8061259
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110782"
---
# <span data-ttu-id="60c84-101">Get-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="60c84-101">Get-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="60c84-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60c84-102">SYNOPSIS</span></span>
<span data-ttu-id="60c84-103">Obtém ou lista a política de replicação de objetos de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="60c84-103">Gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="60c84-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60c84-104">SYNTAX</span></span>

### <span data-ttu-id="60c84-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="60c84-105">AccountName (Default)</span></span>
```
Get-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60c84-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="60c84-106">AccountObject</span></span>
```
Get-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60c84-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="60c84-107">DESCRIPTION</span></span>
<span data-ttu-id="60c84-108">O cmdlet **Get-AzStorageObjectReplicationPolicy** Obtém ou lista a política de replicação de objetos de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="60c84-108">The **Get-AzStorageObjectReplicationPolicy** cmdlet gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="60c84-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60c84-109">EXAMPLES</span></span>

### <span data-ttu-id="60c84-110">Exemplo 1: obter uma política de replicação de objetos com uma ID de política específica e mostrar suas regras.</span><span class="sxs-lookup"><span data-stu-id="60c84-110">Example 1: Get an object replication policy with specific policy Id and show its rules.</span></span>
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

<span data-ttu-id="60c84-111">Este comando obtém uma política de replicação de objetos com uma ID de política específica e mostra suas regras.</span><span class="sxs-lookup"><span data-stu-id="60c84-111">This command gets an object replication policy with specific policy Id and show its rules.</span></span>

### <span data-ttu-id="60c84-112">Exemplo 2: listar a política de replicação de objetos de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="60c84-112">Example 2:List object replication policy from a Storage account</span></span>
```
PS C:\> $policies = Get-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" 

PS C:\> $policies

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysrcaccount1   mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]
myresourcegroup   mydestaccount      68434c7a-20d0-4282-b75c-43b5a243435e             mysrcaccount2   mydestaccount      [d3d39a01-8d92-40e5-849f-e56209ae5cf5,...]
```

<span data-ttu-id="60c84-113">Este comando lista a política de replicação de objetos de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="60c84-113">This command lists object replication policy from a Storage account.</span></span>

## <span data-ttu-id="60c84-114">OS</span><span class="sxs-lookup"><span data-stu-id="60c84-114">PARAMETERS</span></span>

### <span data-ttu-id="60c84-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60c84-115">-DefaultProfile</span></span>
<span data-ttu-id="60c84-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="60c84-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60c84-117">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="60c84-117">-PolicyId</span></span>
<span data-ttu-id="60c84-118">ID da política de replicação de objetos.</span><span class="sxs-lookup"><span data-stu-id="60c84-118">Object Replication Policy Id.</span></span>

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

### <span data-ttu-id="60c84-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60c84-119">-ResourceGroupName</span></span>
<span data-ttu-id="60c84-120">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="60c84-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="60c84-121">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="60c84-121">-StorageAccount</span></span>
<span data-ttu-id="60c84-122">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="60c84-122">Storage account object</span></span>

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

### <span data-ttu-id="60c84-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="60c84-123">-StorageAccountName</span></span>
<span data-ttu-id="60c84-124">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="60c84-124">Storage Account Name.</span></span>

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

### <span data-ttu-id="60c84-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60c84-125">CommonParameters</span></span>
<span data-ttu-id="60c84-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60c84-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60c84-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60c84-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60c84-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="60c84-128">INPUTS</span></span>

### <span data-ttu-id="60c84-129">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="60c84-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="60c84-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="60c84-130">OUTPUTS</span></span>

### <span data-ttu-id="60c84-131">Microsoft. Azure. Commands. Management. Storage. Models. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="60c84-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="60c84-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="60c84-132">NOTES</span></span>

## <span data-ttu-id="60c84-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60c84-133">RELATED LINKS</span></span>
