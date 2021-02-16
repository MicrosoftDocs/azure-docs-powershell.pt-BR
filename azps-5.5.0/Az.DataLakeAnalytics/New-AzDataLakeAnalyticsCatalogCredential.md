---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: BB6AF5A9-49BD-4A76-9F3F-44B62D2AB842
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 4f7a391228529cdb28951b6b3f3f792e8d0de395
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117732"
---
# <span data-ttu-id="18355-101">New-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="18355-101">New-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="18355-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18355-102">SYNOPSIS</span></span>
<span data-ttu-id="18355-103">Cria uma nova credencial de catálogo do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="18355-103">Creates a new Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="18355-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18355-104">SYNTAX</span></span>

### <span data-ttu-id="18355-105">CreateByHostNameAndPort (Padrão)</span><span class="sxs-lookup"><span data-stu-id="18355-105">CreateByHostNameAndPort (Default)</span></span>
```
New-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18355-106">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="18355-106">CreateByFullURI</span></span>
```
New-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-DatabaseHost] <String> [-Port] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18355-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="18355-107">DESCRIPTION</span></span>
<span data-ttu-id="18355-108">O New-AzDataLakeAnalyticsCatalogCredential cmdlet cria uma nova credencial a ser usada em um catálogo do Azure Data Lake Analytics para se conectar a fontes de dados externas.</span><span class="sxs-lookup"><span data-stu-id="18355-108">The New-AzDataLakeAnalyticsCatalogCredential cmdlet creates a new credential to use in an Azure Data Lake Analytics catalog for connecting to external data sources.</span></span>

## <span data-ttu-id="18355-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="18355-109">EXAMPLES</span></span>

### <span data-ttu-id="18355-110">Exemplo 1: Criar uma credencial para um catálogo que especifica o host e a porta</span><span class="sxs-lookup"><span data-stu-id="18355-110">Example 1: Create a credential for a catalog specifying host and port</span></span>
```
PS C:\> New-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -DatabaseHost "example.contoso.com" -Port 8080
```

<span data-ttu-id="18355-111">Esse comando cria a credencial especificada para a conta, o banco de dados, o host e a porta especificadas usando o protocolo https.</span><span class="sxs-lookup"><span data-stu-id="18355-111">This command creates the specified credential for the specified account, database, host and port using https protocol.</span></span>

### <span data-ttu-id="18355-112">Exemplo 2: Criar uma credencial para um catálogo que especifica URI completo</span><span class="sxs-lookup"><span data-stu-id="18355-112">Example 2: Create a credential for a catalog specifying full URI</span></span>
```
PS C:\> New-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -Uri "http://httpExample.contoso.com:8080"
```

<span data-ttu-id="18355-113">Esse comando cria a credencial especificada para o URI de fonte de dados, banco de dados e conta especificada.</span><span class="sxs-lookup"><span data-stu-id="18355-113">This command creates the specified credential for the specified account, database and external data source URI.</span></span>

## <span data-ttu-id="18355-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18355-114">PARAMETERS</span></span>

### <span data-ttu-id="18355-115">-Conta</span><span class="sxs-lookup"><span data-stu-id="18355-115">-Account</span></span>
<span data-ttu-id="18355-116">Especifica o nome da conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="18355-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="18355-117">-Credencial</span><span class="sxs-lookup"><span data-stu-id="18355-117">-Credential</span></span>
<span data-ttu-id="18355-118">Especifica o nome de usuário e a senha correspondente da credencial.</span><span class="sxs-lookup"><span data-stu-id="18355-118">Specifies the user name and corresponding password of the credential.</span></span>

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

### <span data-ttu-id="18355-119">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="18355-119">-CredentialName</span></span>
<span data-ttu-id="18355-120">Especifica o nome e a senha da credencial.</span><span class="sxs-lookup"><span data-stu-id="18355-120">Specifies the name and password of the credential.</span></span>

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

### <span data-ttu-id="18355-121">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="18355-121">-DatabaseHost</span></span>
<span data-ttu-id="18355-122">Especifica o nome do host da fonte de dados externa à que a credencial pode se conectar no formato mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="18355-122">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

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

### <span data-ttu-id="18355-123">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="18355-123">-DatabaseName</span></span>
<span data-ttu-id="18355-124">Especifica o nome do banco de dados na conta do Data Lake Analytics em que a credencial será armazenada.</span><span class="sxs-lookup"><span data-stu-id="18355-124">Specifies the name of the database in the Data Lake Analytics account that the credential will be stored in.</span></span>

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

### <span data-ttu-id="18355-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18355-125">-DefaultProfile</span></span>
<span data-ttu-id="18355-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="18355-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18355-127">-Porta</span><span class="sxs-lookup"><span data-stu-id="18355-127">-Port</span></span>
<span data-ttu-id="18355-128">Especifica o número da porta usada para se conectar ao DatabaseHost especificado usando essa credencial.</span><span class="sxs-lookup"><span data-stu-id="18355-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

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

### <span data-ttu-id="18355-129">-Uri</span><span class="sxs-lookup"><span data-stu-id="18355-129">-Uri</span></span>
<span data-ttu-id="18355-130">Especifica o URI (Uniform Resource Identifier) completo da fonte de dados externa à que essa credencial pode se conectar.</span><span class="sxs-lookup"><span data-stu-id="18355-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

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

### <span data-ttu-id="18355-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="18355-131">-Confirm</span></span>
<span data-ttu-id="18355-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18355-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18355-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18355-133">-WhatIf</span></span>
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

### <span data-ttu-id="18355-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18355-134">CommonParameters</span></span>
<span data-ttu-id="18355-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18355-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18355-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18355-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18355-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="18355-137">INPUTS</span></span>

### <span data-ttu-id="18355-138">System.String</span><span class="sxs-lookup"><span data-stu-id="18355-138">System.String</span></span>

### <span data-ttu-id="18355-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="18355-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="18355-140">System.Uri</span><span class="sxs-lookup"><span data-stu-id="18355-140">System.Uri</span></span>

### <span data-ttu-id="18355-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="18355-141">System.Int32</span></span>

## <span data-ttu-id="18355-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="18355-142">OUTPUTS</span></span>

### <span data-ttu-id="18355-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span><span class="sxs-lookup"><span data-stu-id="18355-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="18355-144">Notas</span><span class="sxs-lookup"><span data-stu-id="18355-144">NOTES</span></span>

## <span data-ttu-id="18355-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18355-145">RELATED LINKS</span></span>
