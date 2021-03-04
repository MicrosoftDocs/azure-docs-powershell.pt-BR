---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
ms.openlocfilehash: dbabc98a8221cc2b870368b2b9cdd55e81280863
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890895"
---
# <span data-ttu-id="697a3-101">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="697a3-101">Get-AzApiManagementPolicy</span></span>

## <span data-ttu-id="697a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="697a3-102">SYNOPSIS</span></span>
<span data-ttu-id="697a3-103">Obtém a política de escopo especificada.</span><span class="sxs-lookup"><span data-stu-id="697a3-103">Gets the specified scope policy.</span></span>

## <span data-ttu-id="697a3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="697a3-104">SYNTAX</span></span>

### <span data-ttu-id="697a3-105">GetTenantLevel (Padrão)</span><span class="sxs-lookup"><span data-stu-id="697a3-105">GetTenantLevel (Default)</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="697a3-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="697a3-106">GetProductLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="697a3-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="697a3-107">GetApiLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="697a3-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="697a3-108">GetOperationLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="697a3-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="697a3-109">DESCRIPTION</span></span>
<span data-ttu-id="697a3-110">O cmdlet **Get-AzApiManagementPolicy** obtém a política de escopo especificada.</span><span class="sxs-lookup"><span data-stu-id="697a3-110">The **Get-AzApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="697a3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="697a3-111">EXAMPLES</span></span>

### <span data-ttu-id="697a3-112">Exemplo 1: Obter a política de nível de locatário</span><span class="sxs-lookup"><span data-stu-id="697a3-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="697a3-113">Este comando obtém a política de nível de locatário e a salva em um arquivo chamado tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="697a3-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="697a3-114">Exemplo 2: Obter a política de escopo do produto</span><span class="sxs-lookup"><span data-stu-id="697a3-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="697a3-115">Este comando obtém a política de escopo do produto</span><span class="sxs-lookup"><span data-stu-id="697a3-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="697a3-116">Exemplo 3: Obter a política de escopo da API</span><span class="sxs-lookup"><span data-stu-id="697a3-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="697a3-117">Este comando obtém a política de escopo da API.</span><span class="sxs-lookup"><span data-stu-id="697a3-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="697a3-118">Exemplo 4: Obter a política de escopo de operação</span><span class="sxs-lookup"><span data-stu-id="697a3-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="697a3-119">Este comando obtém a política de escopo de operação.</span><span class="sxs-lookup"><span data-stu-id="697a3-119">This command gets the operation-scope policy.</span></span>

### <span data-ttu-id="697a3-120">Exemplo 5: Obter a política de escopo tenant no formato RawXml</span><span class="sxs-lookup"><span data-stu-id="697a3-120">Example 5: Get the Tenant scope policy in RawXml format</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS c:\> Get-AzApiManagementPolicy -Context $apimContext -Format rawxml

<policies>
        <inbound>
                <set-header name="correlationid" exists-action="skip">
                        <value>@{
                var guidBinary = new byte[16];
                Array.Copy(Guid.NewGuid().ToByteArray(), 0, guidBinary, 0, 10);
                long time = DateTime.Now.Ticks;
                byte[] bytes = new byte[6];
                unchecked
                {
                       bytes[5] = (byte)(time >> 40);
                       bytes[4] = (byte)(time >> 32);
                       bytes[3] = (byte)(time >> 24);
                       bytes[2] = (byte)(time >> 16);
                       bytes[1] = (byte)(time >> 8);
                       bytes[0] = (byte)(time);
                }
                Array.Copy(bytes, 0, guidBinary, 10, 6);
                return new Guid(guidBinary).ToString();
            }
            </value>
                </set-header>
        </inbound>
        <backend>
                <forward-request />
        </backend>
        <outbound />
        <on-error />
</policies>
```

<span data-ttu-id="697a3-121">Este comando obtém a política de escopo de locatário no formato de escape Não Xml.</span><span class="sxs-lookup"><span data-stu-id="697a3-121">This command gets the tenant-scope policy in Non-Xml escaped format.</span></span>

## <span data-ttu-id="697a3-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="697a3-122">PARAMETERS</span></span>

### <span data-ttu-id="697a3-123">-ApiId</span><span class="sxs-lookup"><span data-stu-id="697a3-123">-ApiId</span></span>
<span data-ttu-id="697a3-124">Especifica o identificador da API existente.</span><span class="sxs-lookup"><span data-stu-id="697a3-124">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="697a3-125">Se você especificar esse parâmetro, o cmdlet retornará a política de escopo da API.</span><span class="sxs-lookup"><span data-stu-id="697a3-125">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="697a3-126">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="697a3-126">-ApiRevision</span></span>
<span data-ttu-id="697a3-127">Identificador da Revisão da API.</span><span class="sxs-lookup"><span data-stu-id="697a3-127">Identifier of API Revision.</span></span> <span data-ttu-id="697a3-128">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="697a3-128">This parameter is optional.</span></span> <span data-ttu-id="697a3-129">Se não for especificada, a política será recuperada da revisão da api ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="697a3-129">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="697a3-130">-Context</span><span class="sxs-lookup"><span data-stu-id="697a3-130">-Context</span></span>
<span data-ttu-id="697a3-131">Especifica uma instância de **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="697a3-131">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="697a3-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="697a3-132">-DefaultProfile</span></span>
<span data-ttu-id="697a3-133">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="697a3-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="697a3-134">-Force</span><span class="sxs-lookup"><span data-stu-id="697a3-134">-Force</span></span>
<span data-ttu-id="697a3-135">ps_force</span><span class="sxs-lookup"><span data-stu-id="697a3-135">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="697a3-136">-Format</span><span class="sxs-lookup"><span data-stu-id="697a3-136">-Format</span></span>
<span data-ttu-id="697a3-137">Especifica o formato da política de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="697a3-137">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="697a3-138">O valor padrão para esse parâmetro é "xml".</span><span class="sxs-lookup"><span data-stu-id="697a3-138">The default value for this parameter is "xml".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="697a3-139">-OperationId</span><span class="sxs-lookup"><span data-stu-id="697a3-139">-OperationId</span></span>
<span data-ttu-id="697a3-140">Especifica o identificador da operação de API existente.</span><span class="sxs-lookup"><span data-stu-id="697a3-140">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="697a3-141">Se você especificar esse parâmetro com *ApiId,* o cmdlet retornará a política de escopo de operação.</span><span class="sxs-lookup"><span data-stu-id="697a3-141">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="697a3-142">-ProductId</span><span class="sxs-lookup"><span data-stu-id="697a3-142">-ProductId</span></span>
<span data-ttu-id="697a3-143">Especifica o identificador de um produto existente.</span><span class="sxs-lookup"><span data-stu-id="697a3-143">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="697a3-144">Se você especificar esse parâmetro, o cmdlet retornará a política de escopo do produto.</span><span class="sxs-lookup"><span data-stu-id="697a3-144">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="697a3-145">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="697a3-145">-SaveAs</span></span>
<span data-ttu-id="697a3-146">Especifica o caminho do arquivo para salvar o resultado.</span><span class="sxs-lookup"><span data-stu-id="697a3-146">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="697a3-147">Se você não especificar esse parâmetro, o resultado será canalizou como uma arraia.</span><span class="sxs-lookup"><span data-stu-id="697a3-147">If you do not specify this parameter the result is pipelined as a sting.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="697a3-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="697a3-148">-Confirm</span></span>
<span data-ttu-id="697a3-149">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="697a3-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="697a3-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="697a3-150">-WhatIf</span></span>
<span data-ttu-id="697a3-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="697a3-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="697a3-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="697a3-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="697a3-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="697a3-153">CommonParameters</span></span>
<span data-ttu-id="697a3-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="697a3-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="697a3-155">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="697a3-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="697a3-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="697a3-156">INPUTS</span></span>

### <span data-ttu-id="697a3-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="697a3-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="697a3-158">System.String</span><span class="sxs-lookup"><span data-stu-id="697a3-158">System.String</span></span>

### <span data-ttu-id="697a3-159">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="697a3-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="697a3-160">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="697a3-160">OUTPUTS</span></span>

### <span data-ttu-id="697a3-161">System.String</span><span class="sxs-lookup"><span data-stu-id="697a3-161">System.String</span></span>

## <span data-ttu-id="697a3-162">NOTES</span><span class="sxs-lookup"><span data-stu-id="697a3-162">NOTES</span></span>

## <span data-ttu-id="697a3-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="697a3-163">RELATED LINKS</span></span>

[<span data-ttu-id="697a3-164">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="697a3-164">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)

[<span data-ttu-id="697a3-165">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="697a3-165">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


