---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: C0BE6C8D-37F5-445F-AE15-2CD4F8D8E031
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: 838ebb56f52aa34bc1fe6016a8bf4f4966f4428d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428949"
---
# <span data-ttu-id="2334f-101">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="2334f-101">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="2334f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2334f-102">SYNOPSIS</span></span>
<span data-ttu-id="2334f-103">Cria um segredo de catálogo do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="2334f-103">Creates a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2334f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2334f-104">SYNTAX</span></span>

### <span data-ttu-id="2334f-105">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="2334f-105">CreateByFullURI</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2334f-106">CreateByHostNameAndPort</span><span class="sxs-lookup"><span data-stu-id="2334f-106">CreateByHostNameAndPort</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2334f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2334f-107">DESCRIPTION</span></span>
<span data-ttu-id="2334f-108">O cmdlet **New-AzureRmDataLakeAnalyticsCatalogSecret** cria um segredo para usar em um catálogo do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="2334f-108">The **New-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet creates a secret to use in an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="2334f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2334f-109">EXAMPLES</span></span>

### <span data-ttu-id="2334f-110">Exemplo 1: obter o segredo para um catálogo</span><span class="sxs-lookup"><span data-stu-id="2334f-110">Example 1: Get the secret for a catalog</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="2334f-111">Esse comando obtém o segredo correspondente à conta, ao banco de dados, à credencial e ao host especificados.</span><span class="sxs-lookup"><span data-stu-id="2334f-111">This command gets the secret corresponding to the specified account, database, credential, and host.</span></span>

## <span data-ttu-id="2334f-112">OS</span><span class="sxs-lookup"><span data-stu-id="2334f-112">PARAMETERS</span></span>

### <span data-ttu-id="2334f-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="2334f-113">-Account</span></span>
<span data-ttu-id="2334f-114">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="2334f-114">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2334f-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="2334f-115">-DatabaseHost</span></span>
<span data-ttu-id="2334f-116">Especifica o nome do host do banco de dados ao qual o segredo está associado no formato ' mydatabase.contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="2334f-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

```yaml
Type: String
Parameter Sets: CreateByFullURI
Aliases: Host

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2334f-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2334f-117">-DatabaseName</span></span>
<span data-ttu-id="2334f-118">Especifica o nome do banco de dados que contém o segredo.</span><span class="sxs-lookup"><span data-stu-id="2334f-118">Specifies the name of the database that holds the secret.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2334f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2334f-119">-DefaultProfile</span></span>
<span data-ttu-id="2334f-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2334f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2334f-121">-Porta</span><span class="sxs-lookup"><span data-stu-id="2334f-121">-Port</span></span>
<span data-ttu-id="2334f-122">Especifica o número da porta do segredo.</span><span class="sxs-lookup"><span data-stu-id="2334f-122">Specifies the port number of the secret.</span></span>

```yaml
Type: Int32
Parameter Sets: CreateByFullURI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2334f-123">-Segredo</span><span class="sxs-lookup"><span data-stu-id="2334f-123">-Secret</span></span>
<span data-ttu-id="2334f-124">Especifica o nome e a senha do segredo.</span><span class="sxs-lookup"><span data-stu-id="2334f-124">Specifies the name and password of the secret.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2334f-125">-URI</span><span class="sxs-lookup"><span data-stu-id="2334f-125">-Uri</span></span>
<span data-ttu-id="2334f-126">Especifica o URI (Uniform Resource Identifier) do segredo.</span><span class="sxs-lookup"><span data-stu-id="2334f-126">Specifies the Uniform Resource Identifier (URI) of the secret.</span></span>

```yaml
Type: Uri
Parameter Sets: CreateByHostNameAndPort
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2334f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2334f-127">CommonParameters</span></span>
<span data-ttu-id="2334f-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2334f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2334f-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2334f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2334f-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2334f-130">INPUTS</span></span>

### <span data-ttu-id="2334f-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2334f-131">None</span></span>
<span data-ttu-id="2334f-132">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="2334f-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2334f-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2334f-133">OUTPUTS</span></span>

### <span data-ttu-id="2334f-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2334f-134">None</span></span>

## <span data-ttu-id="2334f-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2334f-135">NOTES</span></span>

## <span data-ttu-id="2334f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2334f-136">RELATED LINKS</span></span>

[<span data-ttu-id="2334f-137">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="2334f-137">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="2334f-138">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="2334f-138">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)


