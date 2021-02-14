---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/add-azanalysisservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
ms.openlocfilehash: f1d59a0a34072a91242c6595c269ba55c4397e0e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116660"
---
# <span data-ttu-id="517cb-101">Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="517cb-101">Add-AzAnalysisServicesAccount</span></span>

## <span data-ttu-id="517cb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="517cb-102">SYNOPSIS</span></span>
<span data-ttu-id="517cb-103">Adiciona uma conta autenticada a ser usada para solicitações de cmdlet do servidor do Azure Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="517cb-103">Adds an authenticated account to use for Azure Analysis Services server cmdlet requests.</span></span>

## <span data-ttu-id="517cb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="517cb-104">SYNTAX</span></span>

### <span data-ttu-id="517cb-105">UserParameterSetName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="517cb-105">UserParameterSetName (Default)</span></span>
```
Add-AzAnalysisServicesAccount [[-RolloutEnvironment] <String>] [[-Credential] <PSCredential>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="517cb-106">ServicePrincipalWithPasswordParameterSetName</span><span class="sxs-lookup"><span data-stu-id="517cb-106">ServicePrincipalWithPasswordParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="517cb-107">ServicePrincipalWithCertificateParameterSetName</span><span class="sxs-lookup"><span data-stu-id="517cb-107">ServicePrincipalWithCertificateParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-ServicePrincipal] -TenantId <String>
 -ApplicationId <String> -CertificateThumbprint <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="517cb-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="517cb-108">DESCRIPTION</span></span>
<span data-ttu-id="517cb-109">O Add-AzAnalysisServicesAccount cmdlet é usado para fazer logon em uma instância do servidor do Azure Analysis Services</span><span class="sxs-lookup"><span data-stu-id="517cb-109">The Add-AzAnalysisServicesAccount cmdlet is used to login to an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="517cb-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="517cb-110">EXAMPLES</span></span>

### <span data-ttu-id="517cb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="517cb-111">Example 1</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount
RolloutEnvironment: westcentralus.asazure.windows.net
Credential: $UserCredential
```

<span data-ttu-id="517cb-112">Este exemplo adicionará a conta especificada pela variável $UserCredential ao ambiente westcentralus.asazure.windows.net Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="517cb-112">This example will add the account specified by the $UserCredential variable to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="517cb-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="517cb-113">Example 2</span></span>
```
PS C:\>$ApplicationCredential = Get-Credential
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -Credential $ApplicationCredential -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="517cb-114">O primeiro comando obtém as credenciais de entidade de serviço do aplicativo e as armazena na variável $ApplicationCredential aplicativo.</span><span class="sxs-lookup"><span data-stu-id="517cb-114">The first command gets the application service principal credentials, and then stores them in the $ApplicationCredential variable.</span></span>
<span data-ttu-id="517cb-115">O segundo comando adiciona a conta principal de serviço de aplicativo especificada pela variável $ApplicationCredential e TenantId ao ambiente westcentralus.asazure.windows.net Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="517cb-115">The second command add the application service principal account specified by the $ApplicationCredential variable and TenantId to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="517cb-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="517cb-116">Example 3</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -ApplicationId "yyyy-yyyy-yyyy-yyyy" -CertificateThumbprint 'zzzzzzzzzzzzzzzz' -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="517cb-117">Este exemplo adicionará a conta principal do serviço de aplicativo especificada pelo ApplicationId, TenantId e CertificateThumbprint ao ambiente westcentralus.asazure.windows.net Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="517cb-117">This example will add the application service principal account specified by the ApplicationId, TenantId and CertificateThumbprint to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

## <span data-ttu-id="517cb-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="517cb-118">PARAMETERS</span></span>

### <span data-ttu-id="517cb-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="517cb-119">-ApplicationId</span></span>
<span data-ttu-id="517cb-120">A ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="517cb-120">The application ID.</span></span>

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

### <span data-ttu-id="517cb-121">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="517cb-121">-CertificateThumbprint</span></span>
<span data-ttu-id="517cb-122">Hash de certificado (impressão digital)</span><span class="sxs-lookup"><span data-stu-id="517cb-122">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="517cb-123">-Credencial</span><span class="sxs-lookup"><span data-stu-id="517cb-123">-Credential</span></span>
<span data-ttu-id="517cb-124">Credenciais de logon</span><span class="sxs-lookup"><span data-stu-id="517cb-124">Login credentials</span></span>

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

### <span data-ttu-id="517cb-125">-RolloutEnvironment</span><span class="sxs-lookup"><span data-stu-id="517cb-125">-RolloutEnvironment</span></span>
<span data-ttu-id="517cb-126">Nome do ambiente do Azure Analysis Services para o qual fazer logon.</span><span class="sxs-lookup"><span data-stu-id="517cb-126">Name of the Azure Analysis Services environment to which to logon to.</span></span> <span data-ttu-id="517cb-127">Dado o nome completo do servidor, por exemplo, asazure://westcentralus.asazure.windows.net/testserver, o valor correto dessa variável será westcentralus.asazure.windows.net</span><span class="sxs-lookup"><span data-stu-id="517cb-127">Given the full name of the server for example asazure://westcentralus.asazure.windows.net/testserver , the correct value for this variable will be westcentralus.asazure.windows.net</span></span>

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

### <span data-ttu-id="517cb-128">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="517cb-128">-ServicePrincipal</span></span>
<span data-ttu-id="517cb-129">Indica que essa conta autentica fornece credenciais de entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="517cb-129">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="517cb-130">-TenantId</span><span class="sxs-lookup"><span data-stu-id="517cb-130">-TenantId</span></span>
<span data-ttu-id="517cb-131">Nome do locatário ou ID</span><span class="sxs-lookup"><span data-stu-id="517cb-131">Tenant name or ID</span></span>

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

### <span data-ttu-id="517cb-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="517cb-132">-Confirm</span></span>
<span data-ttu-id="517cb-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="517cb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="517cb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="517cb-134">-WhatIf</span></span>
<span data-ttu-id="517cb-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="517cb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="517cb-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="517cb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="517cb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="517cb-137">CommonParameters</span></span>
<span data-ttu-id="517cb-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="517cb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="517cb-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="517cb-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="517cb-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="517cb-140">INPUTS</span></span>

### <span data-ttu-id="517cb-141">Nenhum</span><span class="sxs-lookup"><span data-stu-id="517cb-141">None</span></span>

## <span data-ttu-id="517cb-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="517cb-142">OUTPUTS</span></span>

### <span data-ttu-id="517cb-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span><span class="sxs-lookup"><span data-stu-id="517cb-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span></span>

## <span data-ttu-id="517cb-144">Notas</span><span class="sxs-lookup"><span data-stu-id="517cb-144">NOTES</span></span>
<span data-ttu-id="517cb-145">Alias: Login-AzAsAccount</span><span class="sxs-lookup"><span data-stu-id="517cb-145">Alias: Login-AzAsAccount</span></span>

## <span data-ttu-id="517cb-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="517cb-146">RELATED LINKS</span></span>
