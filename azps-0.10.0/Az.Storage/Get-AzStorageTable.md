---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: 1d06b0934306779d0f8266c24c81810de77b3389
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776246"
---
# <span data-ttu-id="689b1-101">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="689b1-101">Get-AzStorageTable</span></span>

## <span data-ttu-id="689b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="689b1-102">SYNOPSIS</span></span>
<span data-ttu-id="689b1-103">Lista as tabelas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="689b1-103">Lists the storage tables.</span></span>

## <span data-ttu-id="689b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="689b1-104">SYNTAX</span></span>

### <span data-ttu-id="689b1-105">TableName (padrão)</span><span class="sxs-lookup"><span data-stu-id="689b1-105">TableName (Default)</span></span>
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="689b1-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="689b1-106">TablePrefix</span></span>
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="689b1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="689b1-107">DESCRIPTION</span></span>
<span data-ttu-id="689b1-108">O cmdlet **Get-AzStorageTable** lista as tabelas de armazenamento associadas à conta de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="689b1-108">The **Get-AzStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="689b1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="689b1-109">EXAMPLES</span></span>

### <span data-ttu-id="689b1-110">Exemplo 1: listar todas as tabelas de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="689b1-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzStorageTable
```

<span data-ttu-id="689b1-111">Este comando obtém todas as tabelas de armazenamento de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="689b1-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="689b1-112">Exemplo 2: listar tabelas de armazenamento do Azure usando um caractere curinga</span><span class="sxs-lookup"><span data-stu-id="689b1-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzStorageTable -Name table*
```

<span data-ttu-id="689b1-113">Esse comando usa um caractere curinga para obter tabelas de armazenamento cujo nome começa com Table.</span><span class="sxs-lookup"><span data-stu-id="689b1-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="689b1-114">Exemplo 3: listar tabelas de armazenamento do Azure usando prefixo de nome de tabela</span><span class="sxs-lookup"><span data-stu-id="689b1-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

<span data-ttu-id="689b1-115">Esse comando usa o parâmetro *prefix* para obter tabelas de armazenamento cujo nome começa com Table.</span><span class="sxs-lookup"><span data-stu-id="689b1-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="689b1-116">OS</span><span class="sxs-lookup"><span data-stu-id="689b1-116">PARAMETERS</span></span>

### <span data-ttu-id="689b1-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="689b1-117">-Context</span></span>
<span data-ttu-id="689b1-118">Especifica o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="689b1-118">Specifies the storage context.</span></span>
<span data-ttu-id="689b1-119">Para criá-la, você pode usar o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="689b1-119">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="689b1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="689b1-120">-DefaultProfile</span></span>
<span data-ttu-id="689b1-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="689b1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="689b1-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="689b1-122">-Name</span></span>
<span data-ttu-id="689b1-123">Especifica o nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="689b1-123">Specifies the table name.</span></span>
<span data-ttu-id="689b1-124">Se o nome da tabela estiver vazio, o cmdlet lista todas as tabelas.</span><span class="sxs-lookup"><span data-stu-id="689b1-124">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="689b1-125">Caso contrário, ele lista todas as tabelas que correspondem ao nome especificado ou o padrão normal Name.</span><span class="sxs-lookup"><span data-stu-id="689b1-125">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

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

### <span data-ttu-id="689b1-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="689b1-126">-Prefix</span></span>
<span data-ttu-id="689b1-127">Especifica um prefixo usado no nome da tabela ou tabelas que você deseja obter.</span><span class="sxs-lookup"><span data-stu-id="689b1-127">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="689b1-128">Você pode usar isso para localizar todas as tabelas que começam com a mesma cadeia de caracteres, como Table.</span><span class="sxs-lookup"><span data-stu-id="689b1-128">You can use this to find all tables that start with the same string, such as table.</span></span>

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

### <span data-ttu-id="689b1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="689b1-129">CommonParameters</span></span>
<span data-ttu-id="689b1-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="689b1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="689b1-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="689b1-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="689b1-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="689b1-132">INPUTS</span></span>

### <span data-ttu-id="689b1-133">System. String</span><span class="sxs-lookup"><span data-stu-id="689b1-133">System.String</span></span>

### <span data-ttu-id="689b1-134">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="689b1-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="689b1-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="689b1-135">OUTPUTS</span></span>

### <span data-ttu-id="689b1-136">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="689b1-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="689b1-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="689b1-137">NOTES</span></span>

## <span data-ttu-id="689b1-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="689b1-138">RELATED LINKS</span></span>

[<span data-ttu-id="689b1-139">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="689b1-139">New-AzStorageTable</span></span>](./New-AzStorageTable.md)

[<span data-ttu-id="689b1-140">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="689b1-140">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


