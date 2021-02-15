---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 75E4E0FB-35A8-47DA-B606-45E073D04625
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 8d188e2f19c04792ea29cadef9d9ef71c20cfce9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115409"
---
# <span data-ttu-id="0e959-101">Set-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="0e959-101">Set-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="0e959-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0e959-102">SYNOPSIS</span></span>
<span data-ttu-id="0e959-103">Modifica uma senha de catálogo do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0e959-103">Modifies an Azure Data Lake Analytics catalog credential password.</span></span>

## <span data-ttu-id="0e959-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e959-104">SYNTAX</span></span>

### <span data-ttu-id="0e959-105">SetByHostNameAndPort (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0e959-105">SetByHostNameAndPort (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e959-106">SetByFullURI</span><span class="sxs-lookup"><span data-stu-id="0e959-106">SetByFullURI</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-DatabaseHost] <String>
 [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e959-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e959-107">DESCRIPTION</span></span>
<span data-ttu-id="0e959-108">O Set-AzDataLakeAnalyticsCatalogCredential cmdlet modifica uma senha de credencial associada a um catálogo do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0e959-108">The Set-AzDataLakeAnalyticsCatalogCredential cmdlet modifies a credential password associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="0e959-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0e959-109">EXAMPLES</span></span>

### <span data-ttu-id="0e959-110">Exemplo 1: Modificar a senha de uma credencial associada a uma conta</span><span class="sxs-lookup"><span data-stu-id="0e959-110">Example 1: Modify a credential's password associated with an account</span></span>
```
PS C:\> Set-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "credName" `
                  -Credential (Get-Credential) `
                  -NewPassword (Get-Credential) `
                  -Host "example.contoso.com" -Port 8080
```

<span data-ttu-id="0e959-111">Esse comando define a senha de credencial para a senha especificada no NewPassword.</span><span class="sxs-lookup"><span data-stu-id="0e959-111">This command sets the credential password to the password specified in NewPassword.</span></span>

## <span data-ttu-id="0e959-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e959-112">PARAMETERS</span></span>

### <span data-ttu-id="0e959-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="0e959-113">-Account</span></span>
<span data-ttu-id="0e959-114">Especifica o nome da conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0e959-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="0e959-115">-Credencial</span><span class="sxs-lookup"><span data-stu-id="0e959-115">-Credential</span></span>
<span data-ttu-id="0e959-116">Especifica o nome e a senha atual da credencial a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="0e959-116">Specifies the name and current password of the credential to modify.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e959-117">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="0e959-117">-CredentialName</span></span>
<span data-ttu-id="0e959-118">Especifica o nome da credencial a ser modificado</span><span class="sxs-lookup"><span data-stu-id="0e959-118">Specifies the name of the credential to modify</span></span>

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

### <span data-ttu-id="0e959-119">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="0e959-119">-DatabaseHost</span></span>
<span data-ttu-id="0e959-120">Especifica o nome do host da fonte de dados externa à que a credencial pode se conectar no formato mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="0e959-120">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByFullURI
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e959-121">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="0e959-121">-DatabaseName</span></span>
<span data-ttu-id="0e959-122">Especifica o nome do banco de dados na conta do Data Lake Analytics segurando a credencial.</span><span class="sxs-lookup"><span data-stu-id="0e959-122">Specifies the name of the database in the Data Lake Analytics account holding the credential.</span></span>

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

### <span data-ttu-id="0e959-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e959-123">-DefaultProfile</span></span>
<span data-ttu-id="0e959-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="0e959-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e959-125">-NewPassword</span><span class="sxs-lookup"><span data-stu-id="0e959-125">-NewPassword</span></span>
<span data-ttu-id="0e959-126">Especifica a nova senha da credencial</span><span class="sxs-lookup"><span data-stu-id="0e959-126">Specifies the new password for the credential</span></span>

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

### <span data-ttu-id="0e959-127">-Porta</span><span class="sxs-lookup"><span data-stu-id="0e959-127">-Port</span></span>
<span data-ttu-id="0e959-128">Especifica o número da porta usada para se conectar ao DatabaseHost especificado usando essa credencial.</span><span class="sxs-lookup"><span data-stu-id="0e959-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByFullURI
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e959-129">-Uri</span><span class="sxs-lookup"><span data-stu-id="0e959-129">-Uri</span></span>
<span data-ttu-id="0e959-130">Especifica o URI (Uniform Resource Identifier) completo da fonte de dados externa à que essa credencial pode se conectar.</span><span class="sxs-lookup"><span data-stu-id="0e959-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: SetByHostNameAndPort
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e959-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0e959-131">-Confirm</span></span>
<span data-ttu-id="0e959-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e959-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e959-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e959-133">-WhatIf</span></span>
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

### <span data-ttu-id="0e959-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e959-134">CommonParameters</span></span>
<span data-ttu-id="0e959-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e959-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e959-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e959-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e959-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="0e959-137">INPUTS</span></span>

### <span data-ttu-id="0e959-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0e959-138">System.String</span></span>

### <span data-ttu-id="0e959-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="0e959-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="0e959-140">System.Uri</span><span class="sxs-lookup"><span data-stu-id="0e959-140">System.Uri</span></span>

### <span data-ttu-id="0e959-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="0e959-141">System.Int32</span></span>

## <span data-ttu-id="0e959-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="0e959-142">OUTPUTS</span></span>

### <span data-ttu-id="0e959-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span><span class="sxs-lookup"><span data-stu-id="0e959-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="0e959-144">Notas</span><span class="sxs-lookup"><span data-stu-id="0e959-144">NOTES</span></span>

## <span data-ttu-id="0e959-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0e959-145">RELATED LINKS</span></span>
