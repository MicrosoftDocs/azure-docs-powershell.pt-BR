---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/add-azanalysisservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
ms.openlocfilehash: 523ccfb44d29473e41560de88d34519f98272375
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901521"
---
# <span data-ttu-id="8d896-101">Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8d896-101">Add-AzAnalysisServicesAccount</span></span>

## <span data-ttu-id="8d896-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d896-102">SYNOPSIS</span></span>
<span data-ttu-id="8d896-103">Adiciona uma conta autenticada a ser usada para solicitações de cmdlet do servidor do Azure Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="8d896-103">Adds an authenticated account to use for Azure Analysis Services server cmdlet requests.</span></span>

## <span data-ttu-id="8d896-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8d896-104">SYNTAX</span></span>

### <span data-ttu-id="8d896-105">UserParameterSetName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8d896-105">UserParameterSetName (Default)</span></span>
```
Add-AzAnalysisServicesAccount [[-RolloutEnvironment] <String>] [[-Credential] <PSCredential>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d896-106">ServicePrincipalWithPasswordParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8d896-106">ServicePrincipalWithPasswordParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d896-107">ServicePrincipalWithCertificateParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8d896-107">ServicePrincipalWithCertificateParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-ServicePrincipal] -TenantId <String>
 -ApplicationId <String> -CertificateThumbprint <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d896-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8d896-108">DESCRIPTION</span></span>
<span data-ttu-id="8d896-109">O Add-AzAnalysisServicesAccount cmdlet é usado para fazer logon em uma instância do servidor do Azure Analysis Services</span><span class="sxs-lookup"><span data-stu-id="8d896-109">The Add-AzAnalysisServicesAccount cmdlet is used to login to an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="8d896-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d896-110">EXAMPLES</span></span>

### <span data-ttu-id="8d896-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8d896-111">Example 1</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount
RolloutEnvironment: westcentralus.asazure.windows.net
Credential: $UserCredential
```

<span data-ttu-id="8d896-112">Este exemplo adicionará a conta especificada pela variável $UserCredential ao ambiente westcentralus.asazure.windows.net Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="8d896-112">This example will add the account specified by the $UserCredential variable to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="8d896-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8d896-113">Example 2</span></span>
```
PS C:\>$ApplicationCredential = Get-Credential
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -Credential $ApplicationCredential -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="8d896-114">O primeiro comando obtém as credenciais principais do serviço de aplicativo e as armazena na variável $ApplicationCredential aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8d896-114">The first command gets the application service principal credentials, and then stores them in the $ApplicationCredential variable.</span></span>
<span data-ttu-id="8d896-115">O segundo comando adiciona a conta principal do serviço de aplicativo especificada pela variável $ApplicationCredential e TenantId ao ambiente westcentralus.asazure.windows.net Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="8d896-115">The second command add the application service principal account specified by the $ApplicationCredential variable and TenantId to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="8d896-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="8d896-116">Example 3</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -ApplicationId "yyyy-yyyy-yyyy-yyyy" -CertificateThumbprint 'zzzzzzzzzzzzzzzz' -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="8d896-117">Este exemplo adicionará a conta principal do serviço de aplicativo especificada pelo ApplicationId, TenantId e CertificateThumbprint ao ambiente westcentralus.asazure.windows.net Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="8d896-117">This example will add the application service principal account specified by the ApplicationId, TenantId and CertificateThumbprint to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

## <span data-ttu-id="8d896-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8d896-118">PARAMETERS</span></span>

### <span data-ttu-id="8d896-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8d896-119">-ApplicationId</span></span>
<span data-ttu-id="8d896-120">A ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8d896-120">The application ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d896-121">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="8d896-121">-CertificateThumbprint</span></span>
<span data-ttu-id="8d896-122">Hash de certificado (impressão digital)</span><span class="sxs-lookup"><span data-stu-id="8d896-122">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d896-123">-Credential</span><span class="sxs-lookup"><span data-stu-id="8d896-123">-Credential</span></span>
<span data-ttu-id="8d896-124">Credenciais de logon</span><span class="sxs-lookup"><span data-stu-id="8d896-124">Login credentials</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: UserParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithPasswordParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d896-125">-RolloutEnvironment</span><span class="sxs-lookup"><span data-stu-id="8d896-125">-RolloutEnvironment</span></span>
<span data-ttu-id="8d896-126">Nome do ambiente dos Serviços de Análise do Azure para o qual fazer logon.</span><span class="sxs-lookup"><span data-stu-id="8d896-126">Name of the Azure Analysis Services environment to which to logon to.</span></span> <span data-ttu-id="8d896-127">Dado o nome completo do servidor, por exemplo, asazure://westcentralus.asazure.windows.net/testserver , o valor correto para essa variável será westcentralus.asazure.windows.net</span><span class="sxs-lookup"><span data-stu-id="8d896-127">Given the full name of the server for example asazure://westcentralus.asazure.windows.net/testserver , the correct value for this variable will be westcentralus.asazure.windows.net</span></span>

```yaml
Type: System.String
Parameter Sets: UserParameterSetName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d896-128">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8d896-128">-ServicePrincipal</span></span>
<span data-ttu-id="8d896-129">Indica que essa conta é autenticada fornecendo credenciais de entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="8d896-129">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d896-130">-TenantId</span><span class="sxs-lookup"><span data-stu-id="8d896-130">-TenantId</span></span>
<span data-ttu-id="8d896-131">Nome do locatário ou ID</span><span class="sxs-lookup"><span data-stu-id="8d896-131">Tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d896-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d896-132">-Confirm</span></span>
<span data-ttu-id="8d896-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d896-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d896-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d896-134">-WhatIf</span></span>
<span data-ttu-id="8d896-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8d896-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d896-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8d896-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d896-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d896-137">CommonParameters</span></span>
<span data-ttu-id="8d896-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d896-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d896-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d896-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d896-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d896-140">INPUTS</span></span>

### <span data-ttu-id="8d896-141">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8d896-141">None</span></span>

## <span data-ttu-id="8d896-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8d896-142">OUTPUTS</span></span>

### <span data-ttu-id="8d896-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span><span class="sxs-lookup"><span data-stu-id="8d896-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span></span>

## <span data-ttu-id="8d896-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="8d896-144">NOTES</span></span>
<span data-ttu-id="8d896-145">Alias: Login-AzAsAccount</span><span class="sxs-lookup"><span data-stu-id="8d896-145">Alias: Login-AzAsAccount</span></span>

## <span data-ttu-id="8d896-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d896-146">RELATED LINKS</span></span>
