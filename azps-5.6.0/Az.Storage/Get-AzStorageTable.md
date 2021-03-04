---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: d4296acd16b29640fa8925d8482cca012be27b73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890921"
---
# <span data-ttu-id="f05fb-101">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="f05fb-101">Get-AzStorageTable</span></span>

## <span data-ttu-id="f05fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f05fb-102">SYNOPSIS</span></span>
<span data-ttu-id="f05fb-103">Lista as tabelas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f05fb-103">Lists the storage tables.</span></span>

## <span data-ttu-id="f05fb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f05fb-104">SYNTAX</span></span>

### <span data-ttu-id="f05fb-105">TableName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f05fb-105">TableName (Default)</span></span>
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f05fb-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="f05fb-106">TablePrefix</span></span>
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f05fb-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f05fb-107">DESCRIPTION</span></span>
<span data-ttu-id="f05fb-108">O cmdlet **Get-AzStorageTable** lista as tabelas de armazenamento associadas à conta de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="f05fb-108">The **Get-AzStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="f05fb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f05fb-109">EXAMPLES</span></span>

### <span data-ttu-id="f05fb-110">Exemplo 1: Listar todas as tabelas de Armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="f05fb-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzStorageTable
```

<span data-ttu-id="f05fb-111">Este comando obtém todas as tabelas de armazenamento de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f05fb-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="f05fb-112">Exemplo 2: Listar tabelas de armazenamento do Azure usando um caractere curinga</span><span class="sxs-lookup"><span data-stu-id="f05fb-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzStorageTable -Name table*
```

<span data-ttu-id="f05fb-113">Este comando usa um caractere curinga para obter tabelas de armazenamento cujo nome começa com tabela.</span><span class="sxs-lookup"><span data-stu-id="f05fb-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="f05fb-114">Exemplo 3: Listar tabelas de armazenamento do Azure usando prefixo de nome de tabela</span><span class="sxs-lookup"><span data-stu-id="f05fb-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

<span data-ttu-id="f05fb-115">Este comando usa o *parâmetro Prefix* para obter tabelas de armazenamento cujo nome começa com tabela.</span><span class="sxs-lookup"><span data-stu-id="f05fb-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="f05fb-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f05fb-116">PARAMETERS</span></span>

### <span data-ttu-id="f05fb-117">-Context</span><span class="sxs-lookup"><span data-stu-id="f05fb-117">-Context</span></span>
<span data-ttu-id="f05fb-118">Especifica o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f05fb-118">Specifies the storage context.</span></span>
<span data-ttu-id="f05fb-119">Para criar, você pode usar o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="f05fb-119">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f05fb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f05fb-120">-DefaultProfile</span></span>
<span data-ttu-id="f05fb-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f05fb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f05fb-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f05fb-122">-Name</span></span>
<span data-ttu-id="f05fb-123">Especifica o nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="f05fb-123">Specifies the table name.</span></span>
<span data-ttu-id="f05fb-124">Se o nome da tabela estiver vazio, o cmdlet lista todas as tabelas.</span><span class="sxs-lookup"><span data-stu-id="f05fb-124">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="f05fb-125">Caso contrário, lista todas as tabelas que corresponderem ao nome especificado ou ao padrão de nome regular.</span><span class="sxs-lookup"><span data-stu-id="f05fb-125">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f05fb-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="f05fb-126">-Prefix</span></span>
<span data-ttu-id="f05fb-127">Especifica um prefixo usado no nome da tabela ou tabelas que você deseja obter.</span><span class="sxs-lookup"><span data-stu-id="f05fb-127">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="f05fb-128">Você pode usar isso para encontrar todas as tabelas que começam com a mesma cadeia de caracteres, como tabela.</span><span class="sxs-lookup"><span data-stu-id="f05fb-128">You can use this to find all tables that start with the same string, such as table.</span></span>

```yaml
Type: System.String
Parameter Sets: TablePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f05fb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f05fb-129">CommonParameters</span></span>
<span data-ttu-id="f05fb-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f05fb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f05fb-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f05fb-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f05fb-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f05fb-132">INPUTS</span></span>

### <span data-ttu-id="f05fb-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f05fb-133">System.String</span></span>

### <span data-ttu-id="f05fb-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f05fb-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f05fb-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f05fb-135">OUTPUTS</span></span>

### <span data-ttu-id="f05fb-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="f05fb-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="f05fb-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="f05fb-137">NOTES</span></span>

## <span data-ttu-id="f05fb-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f05fb-138">RELATED LINKS</span></span>

[<span data-ttu-id="f05fb-139">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="f05fb-139">New-AzStorageTable</span></span>](./New-AzStorageTable.md)

[<span data-ttu-id="f05fb-140">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="f05fb-140">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


