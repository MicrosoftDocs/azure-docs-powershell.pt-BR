---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: BB6AF5A9-49BD-4A76-9F3F-44B62D2AB842
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 1668ca10c8c3425bea7c4082033abb19f8de7306
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427959"
---
# <span data-ttu-id="06a97-101">New-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="06a97-101">New-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="06a97-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06a97-102">SYNOPSIS</span></span>
<span data-ttu-id="06a97-103">Cria uma nova credencial de catálogo do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="06a97-103">Creates a new Azure Data Lake Analytics catalog credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06a97-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06a97-104">SYNTAX</span></span>

### <span data-ttu-id="06a97-105">Especificar o nome e a porta do host (padrão)</span><span class="sxs-lookup"><span data-stu-id="06a97-105">Specify host name and port (Default)</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06a97-106">Especificar o URI completo</span><span class="sxs-lookup"><span data-stu-id="06a97-106">Specify full URI</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-DatabaseHost] <String> [-Port] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06a97-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="06a97-107">DESCRIPTION</span></span>
<span data-ttu-id="06a97-108">O cmdlet New-AzureRmDataLakeAnalyticsCatalogCredential cria uma nova credencial para usar em um catálogo do Azure data Lake Analytics para se conectar a fontes de dados externas.</span><span class="sxs-lookup"><span data-stu-id="06a97-108">The New-AzureRmDataLakeAnalyticsCatalogCredential cmdlet creates a new credential to use in an Azure Data Lake Analytics catalog for connecting to external data sources.</span></span>

## <span data-ttu-id="06a97-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06a97-109">EXAMPLES</span></span>

### <span data-ttu-id="06a97-110">Exemplo 1: criar uma credencial para um catálogo especificando host e porta</span><span class="sxs-lookup"><span data-stu-id="06a97-110">Example 1: Create a credential for a catalog specifying host and port</span></span>
```
PS C:\> New-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -DatabaseHost "example.contoso.com" -Port 8080
```

<span data-ttu-id="06a97-111">Esse comando cria a credencial especificada para a conta, o banco de dados, o host e a porta especificados usando o protocolo HTTPS.</span><span class="sxs-lookup"><span data-stu-id="06a97-111">This command creates the specified credential for the specified account, database, host and port using https protocol.</span></span>

### <span data-ttu-id="06a97-112">Exemplo 2: criar uma credencial para um catálogo especificando o URI completo</span><span class="sxs-lookup"><span data-stu-id="06a97-112">Example 2: Create a credential for a catalog specifying full URI</span></span>
```
PS C:\> New-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -Uri "http://httpExample.contoso.com:8080"
```

<span data-ttu-id="06a97-113">Esse comando cria a credencial especificada para a conta especificada, o banco de dados e o URI da fonte de dados externa.</span><span class="sxs-lookup"><span data-stu-id="06a97-113">This command creates the specified credential for the specified account, database and external data source URI.</span></span>

## <span data-ttu-id="06a97-114">OS</span><span class="sxs-lookup"><span data-stu-id="06a97-114">PARAMETERS</span></span>

### <span data-ttu-id="06a97-115">-Conta</span><span class="sxs-lookup"><span data-stu-id="06a97-115">-Account</span></span>
<span data-ttu-id="06a97-116">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="06a97-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06a97-117">-Credential</span><span class="sxs-lookup"><span data-stu-id="06a97-117">-Credential</span></span>
<span data-ttu-id="06a97-118">Especifica o nome de usuário e a senha correspondente da credencial.</span><span class="sxs-lookup"><span data-stu-id="06a97-118">Specifies the user name and corresponding password of the credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06a97-119">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="06a97-119">-CredentialName</span></span>
<span data-ttu-id="06a97-120">Especifica o nome e a senha da credencial.</span><span class="sxs-lookup"><span data-stu-id="06a97-120">Specifies the name and password of the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06a97-121">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="06a97-121">-DatabaseHost</span></span>
<span data-ttu-id="06a97-122">Especifica o nome do host da fonte de dados externa à qual a credencial pode se conectar no formato mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="06a97-122">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06a97-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="06a97-123">-DatabaseName</span></span>
<span data-ttu-id="06a97-124">Especifica o nome do banco de dados no acocunt data Lake Analytics em que a credencial será armazenada.</span><span class="sxs-lookup"><span data-stu-id="06a97-124">Specifies the name of the database in the Data Lake Analytics acocunt that the credential will be stored in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06a97-125">-Porta</span><span class="sxs-lookup"><span data-stu-id="06a97-125">-Port</span></span>
<span data-ttu-id="06a97-126">Especifica o número da porta usada para se conectar ao DatabaseHost especificado usando essa credencial.</span><span class="sxs-lookup"><span data-stu-id="06a97-126">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06a97-127">-URI</span><span class="sxs-lookup"><span data-stu-id="06a97-127">-Uri</span></span>
<span data-ttu-id="06a97-128">Especifica o URI (Uniform Resource Identifier) completo da fonte de dados externa à qual essa credencial pode se conectar.</span><span class="sxs-lookup"><span data-stu-id="06a97-128">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Specify host name and port
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06a97-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="06a97-129">-Confirm</span></span>
<span data-ttu-id="06a97-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06a97-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06a97-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06a97-131">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06a97-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06a97-132">-DefaultProfile</span></span>
<span data-ttu-id="06a97-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="06a97-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06a97-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06a97-134">CommonParameters</span></span>
<span data-ttu-id="06a97-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06a97-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06a97-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06a97-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06a97-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="06a97-137">INPUTS</span></span>

## <span data-ttu-id="06a97-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="06a97-138">OUTPUTS</span></span>

### <span data-ttu-id="06a97-139">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="06a97-139">None</span></span>

## <span data-ttu-id="06a97-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="06a97-140">NOTES</span></span>

## <span data-ttu-id="06a97-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06a97-141">RELATED LINKS</span></span>

