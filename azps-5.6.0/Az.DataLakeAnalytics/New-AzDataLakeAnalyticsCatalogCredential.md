---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: BB6AF5A9-49BD-4A76-9F3F-44B62D2AB842
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: d5fe98e6c8514ced094700e4633ebbd2e7f1d197
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888254"
---
# <span data-ttu-id="d7e39-101">New-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="d7e39-101">New-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="d7e39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7e39-102">SYNOPSIS</span></span>
<span data-ttu-id="d7e39-103">Cria uma nova credencial de catálogo do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d7e39-103">Creates a new Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="d7e39-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d7e39-104">SYNTAX</span></span>

### <span data-ttu-id="d7e39-105">CreateByHostNameAndPort (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d7e39-105">CreateByHostNameAndPort (Default)</span></span>
```
New-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7e39-106">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="d7e39-106">CreateByFullURI</span></span>
```
New-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-DatabaseHost] <String> [-Port] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7e39-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d7e39-107">DESCRIPTION</span></span>
<span data-ttu-id="d7e39-108">O New-AzDataLakeAnalyticsCatalogCredential cmdlet cria uma nova credencial a ser usada em um catálogo do Azure Data Lake Analytics para se conectar a fontes de dados externas.</span><span class="sxs-lookup"><span data-stu-id="d7e39-108">The New-AzDataLakeAnalyticsCatalogCredential cmdlet creates a new credential to use in an Azure Data Lake Analytics catalog for connecting to external data sources.</span></span>

## <span data-ttu-id="d7e39-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7e39-109">EXAMPLES</span></span>

### <span data-ttu-id="d7e39-110">Exemplo 1: Criar uma credencial para um catálogo especificando host e porta</span><span class="sxs-lookup"><span data-stu-id="d7e39-110">Example 1: Create a credential for a catalog specifying host and port</span></span>
```
PS C:\> New-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -DatabaseHost "example.contoso.com" -Port 8080
```

<span data-ttu-id="d7e39-111">Este comando cria a credencial especificada para a conta, banco de dados, host e porta especificada usando o protocolo https.</span><span class="sxs-lookup"><span data-stu-id="d7e39-111">This command creates the specified credential for the specified account, database, host and port using https protocol.</span></span>

### <span data-ttu-id="d7e39-112">Exemplo 2: Criar uma credencial para um catálogo especificando URI completo</span><span class="sxs-lookup"><span data-stu-id="d7e39-112">Example 2: Create a credential for a catalog specifying full URI</span></span>
```
PS C:\> New-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -Uri "http://httpExample.contoso.com:8080"
```

<span data-ttu-id="d7e39-113">Este comando cria a credencial especificada para a conta especificada, banco de dados e URI de fonte de dados externos.</span><span class="sxs-lookup"><span data-stu-id="d7e39-113">This command creates the specified credential for the specified account, database and external data source URI.</span></span>

## <span data-ttu-id="d7e39-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d7e39-114">PARAMETERS</span></span>

### <span data-ttu-id="d7e39-115">-Account</span><span class="sxs-lookup"><span data-stu-id="d7e39-115">-Account</span></span>
<span data-ttu-id="d7e39-116">Especifica o nome da conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d7e39-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="d7e39-117">-Credential</span><span class="sxs-lookup"><span data-stu-id="d7e39-117">-Credential</span></span>
<span data-ttu-id="d7e39-118">Especifica o nome de usuário e a senha correspondente da credencial.</span><span class="sxs-lookup"><span data-stu-id="d7e39-118">Specifies the user name and corresponding password of the credential.</span></span>

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

### <span data-ttu-id="d7e39-119">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="d7e39-119">-CredentialName</span></span>
<span data-ttu-id="d7e39-120">Especifica o nome e a senha da credencial.</span><span class="sxs-lookup"><span data-stu-id="d7e39-120">Specifies the name and password of the credential.</span></span>

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

### <span data-ttu-id="d7e39-121">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="d7e39-121">-DatabaseHost</span></span>
<span data-ttu-id="d7e39-122">Especifica o nome do host da fonte de dados externa à que a credencial pode se conectar no formato mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="d7e39-122">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByFullURI
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7e39-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d7e39-123">-DatabaseName</span></span>
<span data-ttu-id="d7e39-124">Especifica o nome do banco de dados na conta do Data Lake Analytics em que a credencial será armazenada.</span><span class="sxs-lookup"><span data-stu-id="d7e39-124">Specifies the name of the database in the Data Lake Analytics account that the credential will be stored in.</span></span>

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

### <span data-ttu-id="d7e39-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7e39-125">-DefaultProfile</span></span>
<span data-ttu-id="d7e39-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="d7e39-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7e39-127">-Port</span><span class="sxs-lookup"><span data-stu-id="d7e39-127">-Port</span></span>
<span data-ttu-id="d7e39-128">Especifica o número de porta usado para se conectar ao DatabaseHost especificado usando essa credencial.</span><span class="sxs-lookup"><span data-stu-id="d7e39-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByFullURI
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7e39-129">-Uri</span><span class="sxs-lookup"><span data-stu-id="d7e39-129">-Uri</span></span>
<span data-ttu-id="d7e39-130">Especifica o URI (Uniform Resource Identifier) completo da fonte de dados externa à que essa credencial pode se conectar.</span><span class="sxs-lookup"><span data-stu-id="d7e39-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: CreateByHostNameAndPort
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7e39-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7e39-131">-Confirm</span></span>
<span data-ttu-id="d7e39-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7e39-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7e39-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7e39-133">-WhatIf</span></span>
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

### <span data-ttu-id="d7e39-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7e39-134">CommonParameters</span></span>
<span data-ttu-id="d7e39-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7e39-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7e39-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7e39-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7e39-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7e39-137">INPUTS</span></span>

### <span data-ttu-id="d7e39-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d7e39-138">System.String</span></span>

### <span data-ttu-id="d7e39-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="d7e39-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="d7e39-140">System.Uri</span><span class="sxs-lookup"><span data-stu-id="d7e39-140">System.Uri</span></span>

### <span data-ttu-id="d7e39-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d7e39-141">System.Int32</span></span>

## <span data-ttu-id="d7e39-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d7e39-142">OUTPUTS</span></span>

### <span data-ttu-id="d7e39-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span><span class="sxs-lookup"><span data-stu-id="d7e39-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="d7e39-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="d7e39-144">NOTES</span></span>

## <span data-ttu-id="d7e39-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7e39-145">RELATED LINKS</span></span>
