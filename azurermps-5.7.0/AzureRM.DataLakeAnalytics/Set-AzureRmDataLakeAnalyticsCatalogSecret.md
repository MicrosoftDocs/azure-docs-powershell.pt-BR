---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CAB32C72-5C16-467E-BC57-749EC49916BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: cce57a2437a5e1fa0f440986534a11c1ab6c73ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429815"
---
# <span data-ttu-id="88257-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="88257-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="88257-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88257-102">SYNOPSIS</span></span>
<span data-ttu-id="88257-103">Modifica um segredo de catálogo do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="88257-103">Modifies a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88257-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88257-104">SYNTAX</span></span>

### <span data-ttu-id="88257-105">SetByFullUri</span><span class="sxs-lookup"><span data-stu-id="88257-105">SetByFullUri</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88257-106">SetByHostNameAndPort</span><span class="sxs-lookup"><span data-stu-id="88257-106">SetByHostNameAndPort</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88257-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="88257-107">DESCRIPTION</span></span>
<span data-ttu-id="88257-108">O cmdlet **set-AzureRmDataLakeAnalyticsCatalogSecret** modifica um segredo associado a um catálogo do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="88257-108">The **Set-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet modifies a secret associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="88257-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="88257-109">EXAMPLES</span></span>

### <span data-ttu-id="88257-110">Exemplo 1: modificar o segredo associado a uma conta</span><span class="sxs-lookup"><span data-stu-id="88257-110">Example 1: Modify the secret associated with an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="88257-111">Esse comando define o segredo associado a um catálogo de análise do data Lake.</span><span class="sxs-lookup"><span data-stu-id="88257-111">This command sets the secret associated with a Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="88257-112">OS</span><span class="sxs-lookup"><span data-stu-id="88257-112">PARAMETERS</span></span>

### <span data-ttu-id="88257-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="88257-113">-Account</span></span>
<span data-ttu-id="88257-114">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="88257-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="88257-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="88257-115">-DatabaseHost</span></span>
<span data-ttu-id="88257-116">Especifica o nome do host do banco de dados ao qual o segredo está associado no formato ' mydatabase.contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="88257-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

```yaml
Type: String
Parameter Sets: SetByFullUri
Aliases: Host

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88257-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="88257-117">-DatabaseName</span></span>
<span data-ttu-id="88257-118">Especifica o nome do banco de dados que contém o segredo.</span><span class="sxs-lookup"><span data-stu-id="88257-118">Specifies the name of the database holding the secret.</span></span>

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

### <span data-ttu-id="88257-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88257-119">-DefaultProfile</span></span>
<span data-ttu-id="88257-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="88257-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88257-121">-Porta</span><span class="sxs-lookup"><span data-stu-id="88257-121">-Port</span></span>
<span data-ttu-id="88257-122">Especifica o número da porta do segredo.</span><span class="sxs-lookup"><span data-stu-id="88257-122">Specifies the port number of the secret.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByFullUri
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88257-123">-Segredo</span><span class="sxs-lookup"><span data-stu-id="88257-123">-Secret</span></span>
<span data-ttu-id="88257-124">Especifica o nome e a senha do segredo.</span><span class="sxs-lookup"><span data-stu-id="88257-124">Specifies the name and password of the secret.</span></span>

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

### <span data-ttu-id="88257-125">-URI</span><span class="sxs-lookup"><span data-stu-id="88257-125">-Uri</span></span>
<span data-ttu-id="88257-126">Especifica o URI (Uniform Resource Identifier) do segredo.</span><span class="sxs-lookup"><span data-stu-id="88257-126">Specifies the Uniform Resource Identifier (URI) for the secret.</span></span>

```yaml
Type: Uri
Parameter Sets: SetByHostNameAndPort
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88257-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88257-127">CommonParameters</span></span>
<span data-ttu-id="88257-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88257-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88257-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88257-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88257-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="88257-130">INPUTS</span></span>

### <span data-ttu-id="88257-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="88257-131">None</span></span>
<span data-ttu-id="88257-132">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="88257-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="88257-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="88257-133">OUTPUTS</span></span>

### <span data-ttu-id="88257-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="88257-134">None</span></span>

## <span data-ttu-id="88257-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="88257-135">NOTES</span></span>

## <span data-ttu-id="88257-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88257-136">RELATED LINKS</span></span>

[<span data-ttu-id="88257-137">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="88257-137">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="88257-138">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="88257-138">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)


