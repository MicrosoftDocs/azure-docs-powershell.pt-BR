---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 75E4E0FB-35A8-47DA-B606-45E073D04625
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 534608e2270cd2a3254096dc5b3def7310b7dc4d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770967"
---
# <span data-ttu-id="3671a-101">Set-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="3671a-101">Set-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="3671a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3671a-102">SYNOPSIS</span></span>
<span data-ttu-id="3671a-103">Modifica uma senha de catálogo do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="3671a-103">Modifies an Azure Data Lake Analytics catalog credential password.</span></span>

## <span data-ttu-id="3671a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3671a-104">SYNTAX</span></span>

### <span data-ttu-id="3671a-105">SetByHostNameAndPort (padrão)</span><span class="sxs-lookup"><span data-stu-id="3671a-105">SetByHostNameAndPort (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3671a-106">SetByFullURI</span><span class="sxs-lookup"><span data-stu-id="3671a-106">SetByFullURI</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-DatabaseHost] <String>
 [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3671a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3671a-107">DESCRIPTION</span></span>
<span data-ttu-id="3671a-108">O cmdlet Set-AzDataLakeAnalyticsCatalogCredential modifica uma senha de credencial associada a um catálogo do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="3671a-108">The Set-AzDataLakeAnalyticsCatalogCredential cmdlet modifies a credential password associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="3671a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3671a-109">EXAMPLES</span></span>

### <span data-ttu-id="3671a-110">Exemplo 1: modificar a senha de uma credencial associada a uma conta</span><span class="sxs-lookup"><span data-stu-id="3671a-110">Example 1: Modify a credential's password associated with an account</span></span>
```
PS C:\> Set-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "credName" `
                  -Credential (Get-Credential) `
                  -NewPassword (Get-Credential) `
                  -Host "example.contoso.com" -Port 8080
```

<span data-ttu-id="3671a-111">Este comando define a senha da credencial como a senha especificada em NewPassword.</span><span class="sxs-lookup"><span data-stu-id="3671a-111">This command sets the credential password to the password specified in NewPassword.</span></span>

## <span data-ttu-id="3671a-112">OS</span><span class="sxs-lookup"><span data-stu-id="3671a-112">PARAMETERS</span></span>

### <span data-ttu-id="3671a-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="3671a-113">-Account</span></span>
<span data-ttu-id="3671a-114">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="3671a-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="3671a-115">-Credential</span><span class="sxs-lookup"><span data-stu-id="3671a-115">-Credential</span></span>
<span data-ttu-id="3671a-116">Especifica o nome e a senha atual da credencial a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="3671a-116">Specifies the name and current password of the credential to modify.</span></span>

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

### <span data-ttu-id="3671a-117">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="3671a-117">-CredentialName</span></span>
<span data-ttu-id="3671a-118">Especifica o nome da credencial a ser modificada</span><span class="sxs-lookup"><span data-stu-id="3671a-118">Specifies the name of the credential to modify</span></span>

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

### <span data-ttu-id="3671a-119">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="3671a-119">-DatabaseHost</span></span>
<span data-ttu-id="3671a-120">Especifica o nome do host da fonte de dados externa à qual a credencial pode se conectar no formato mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="3671a-120">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

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

### <span data-ttu-id="3671a-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3671a-121">-DatabaseName</span></span>
<span data-ttu-id="3671a-122">Especifica o nome do banco de dados na conta data Lake Analytics que mantém a credencial.</span><span class="sxs-lookup"><span data-stu-id="3671a-122">Specifies the name of the database in the Data Lake Analytics account holding the credential.</span></span>

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

### <span data-ttu-id="3671a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3671a-123">-DefaultProfile</span></span>
<span data-ttu-id="3671a-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3671a-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3671a-125">-NewPassword</span><span class="sxs-lookup"><span data-stu-id="3671a-125">-NewPassword</span></span>
<span data-ttu-id="3671a-126">Especifica a nova senha da credencial</span><span class="sxs-lookup"><span data-stu-id="3671a-126">Specifies the new password for the credential</span></span>

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

### <span data-ttu-id="3671a-127">-Porta</span><span class="sxs-lookup"><span data-stu-id="3671a-127">-Port</span></span>
<span data-ttu-id="3671a-128">Especifica o número da porta usada para se conectar ao DatabaseHost especificado usando essa credencial.</span><span class="sxs-lookup"><span data-stu-id="3671a-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

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

### <span data-ttu-id="3671a-129">-URI</span><span class="sxs-lookup"><span data-stu-id="3671a-129">-Uri</span></span>
<span data-ttu-id="3671a-130">Especifica o URI (Uniform Resource Identifier) completo da fonte de dados externa à qual essa credencial pode se conectar.</span><span class="sxs-lookup"><span data-stu-id="3671a-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

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

### <span data-ttu-id="3671a-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3671a-131">-Confirm</span></span>
<span data-ttu-id="3671a-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3671a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3671a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3671a-133">-WhatIf</span></span>
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

### <span data-ttu-id="3671a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3671a-134">CommonParameters</span></span>
<span data-ttu-id="3671a-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3671a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3671a-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3671a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3671a-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3671a-137">INPUTS</span></span>

### <span data-ttu-id="3671a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3671a-138">System.String</span></span>

### <span data-ttu-id="3671a-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="3671a-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="3671a-140">System. URI</span><span class="sxs-lookup"><span data-stu-id="3671a-140">System.Uri</span></span>

### <span data-ttu-id="3671a-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3671a-141">System.Int32</span></span>

## <span data-ttu-id="3671a-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3671a-142">OUTPUTS</span></span>

### <span data-ttu-id="3671a-143">Microsoft. Azure. Management. datalake. Analytics. Models. USqlCredential</span><span class="sxs-lookup"><span data-stu-id="3671a-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="3671a-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3671a-144">NOTES</span></span>

## <span data-ttu-id="3671a-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3671a-145">RELATED LINKS</span></span>
