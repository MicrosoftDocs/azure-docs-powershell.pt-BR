---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: d501faaebcc5e381dc2a7270c8b55b148e2812b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115665"
---
# <span data-ttu-id="99ae8-101">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="99ae8-101">Get-AzStorageTable</span></span>

## <span data-ttu-id="99ae8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99ae8-102">SYNOPSIS</span></span>
<span data-ttu-id="99ae8-103">Lista as tabelas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="99ae8-103">Lists the storage tables.</span></span>

## <span data-ttu-id="99ae8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="99ae8-104">SYNTAX</span></span>

### <span data-ttu-id="99ae8-105">Nomeda Tabela (Padrão)</span><span class="sxs-lookup"><span data-stu-id="99ae8-105">TableName (Default)</span></span>
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="99ae8-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="99ae8-106">TablePrefix</span></span>
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99ae8-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="99ae8-107">DESCRIPTION</span></span>
<span data-ttu-id="99ae8-108">O **cmdlet Get-AzStorageTable** lista as tabelas de armazenamento associadas à conta de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="99ae8-108">The **Get-AzStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="99ae8-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="99ae8-109">EXAMPLES</span></span>

### <span data-ttu-id="99ae8-110">Exemplo 1: Listar todas as tabelas de Armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="99ae8-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzStorageTable
```

<span data-ttu-id="99ae8-111">Esse comando obtém todas as tabelas de armazenamento de uma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="99ae8-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="99ae8-112">Exemplo 2: Listar tabelas de armazenamento do Azure usando um caractere curinga</span><span class="sxs-lookup"><span data-stu-id="99ae8-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzStorageTable -Name table*
```

<span data-ttu-id="99ae8-113">Esse comando usa um caractere curinga para obter tabelas de armazenamento cujo nome começa com tabela.</span><span class="sxs-lookup"><span data-stu-id="99ae8-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="99ae8-114">Exemplo 3: Listar tabelas de armazenamento do Azure usando o prefixo de nome de tabela</span><span class="sxs-lookup"><span data-stu-id="99ae8-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

<span data-ttu-id="99ae8-115">Esse comando usa o parâmetro *Prefixo* para obter tabelas de armazenamento cujo nome começa com tabela.</span><span class="sxs-lookup"><span data-stu-id="99ae8-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="99ae8-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99ae8-116">PARAMETERS</span></span>

### <span data-ttu-id="99ae8-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="99ae8-117">-Context</span></span>
<span data-ttu-id="99ae8-118">Especifica o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="99ae8-118">Specifies the storage context.</span></span>
<span data-ttu-id="99ae8-119">Para criar, você pode usar o cmdlet New-AzStorageContext dados.</span><span class="sxs-lookup"><span data-stu-id="99ae8-119">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="99ae8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99ae8-120">-DefaultProfile</span></span>
<span data-ttu-id="99ae8-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="99ae8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99ae8-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="99ae8-122">-Name</span></span>
<span data-ttu-id="99ae8-123">Especifica o nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="99ae8-123">Specifies the table name.</span></span>
<span data-ttu-id="99ae8-124">Se o nome da tabela estiver vazio, o cmdlet lista todas as tabelas.</span><span class="sxs-lookup"><span data-stu-id="99ae8-124">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="99ae8-125">Caso contrário, ele lista todas as tabelas que corresponderem ao nome especificado ou ao padrão de nome normal.</span><span class="sxs-lookup"><span data-stu-id="99ae8-125">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

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

### <span data-ttu-id="99ae8-126">-Prefixo</span><span class="sxs-lookup"><span data-stu-id="99ae8-126">-Prefix</span></span>
<span data-ttu-id="99ae8-127">Especifica um prefixo usado no nome da tabela ou tabelas que você deseja obter.</span><span class="sxs-lookup"><span data-stu-id="99ae8-127">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="99ae8-128">Você pode usá-lo para encontrar todas as tabelas que começam com a mesma cadeia de caracteres, como tabela.</span><span class="sxs-lookup"><span data-stu-id="99ae8-128">You can use this to find all tables that start with the same string, such as table.</span></span>

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

### <span data-ttu-id="99ae8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99ae8-129">CommonParameters</span></span>
<span data-ttu-id="99ae8-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99ae8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99ae8-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99ae8-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99ae8-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="99ae8-132">INPUTS</span></span>

### <span data-ttu-id="99ae8-133">System.String</span><span class="sxs-lookup"><span data-stu-id="99ae8-133">System.String</span></span>

### <span data-ttu-id="99ae8-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="99ae8-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="99ae8-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="99ae8-135">OUTPUTS</span></span>

### <span data-ttu-id="99ae8-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="99ae8-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="99ae8-137">Notas</span><span class="sxs-lookup"><span data-stu-id="99ae8-137">NOTES</span></span>

## <span data-ttu-id="99ae8-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99ae8-138">RELATED LINKS</span></span>

[<span data-ttu-id="99ae8-139">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="99ae8-139">New-AzStorageTable</span></span>](./New-AzStorageTable.md)

[<span data-ttu-id="99ae8-140">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="99ae8-140">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


