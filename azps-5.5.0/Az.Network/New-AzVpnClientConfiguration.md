---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: 11b18f0a0f12a82e88694fd91ce89956951a4eb6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114125"
---
# <span data-ttu-id="eb237-101">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb237-101">New-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="eb237-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eb237-102">SYNOPSIS</span></span>
<span data-ttu-id="eb237-103">Esse comando permite que os usuários criem o pacote de perfil vpn com base nas configurações de vpn pré-configuradas no gateway VPN, além de algumas configurações adicionais que os usuários talvez precisem configurar, por exemplo, alguns certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="eb237-103">This command allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="eb237-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb237-104">SYNTAX</span></span>

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 [-AuthenticationMethod <String>] [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb237-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="eb237-105">DESCRIPTION</span></span>
<span data-ttu-id="eb237-106">Isso permite que os usuários criem o pacote de perfil vpn com base nas configurações de vpn pré-configuradas no gateway VPN, além de algumas configurações adicionais que os usuários podem precisar configurar, por exemplo, alguns certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="eb237-106">this allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="eb237-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="eb237-107">EXAMPLES</span></span>

### <span data-ttu-id="eb237-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="eb237-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

<span data-ttu-id="eb237-109">Este cmdlet é usado para criar um arquivo zip de perfil de cliente VPN para "ContosoVirtualNetworkGateway" no ResourceGroup "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="eb237-109">This cmdlet is used to create a VPN client profile zip file for "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span></span> <span data-ttu-id="eb237-110">O perfil é gerado para um servidor de raio pré-configurado configurado para usar o método de autenticação "EAPTLS" com o arquivo de certificado VpnProfileRadiusCert.</span><span class="sxs-lookup"><span data-stu-id="eb237-110">The profile is generated for a pre-configured radius server that is configured to use "EAPTLS" authentication method with the VpnProfileRadiusCert certificate file.</span></span>

## <span data-ttu-id="eb237-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb237-111">PARAMETERS</span></span>

### <span data-ttu-id="eb237-112">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="eb237-112">-AuthenticationMethod</span></span>
<span data-ttu-id="eb237-113">O Método de Autenticação pode ter valores EAPMSCHAPv2 ou EAPTLS.</span><span class="sxs-lookup"><span data-stu-id="eb237-113">Authentication Method Can take values EAPMSCHAPv2 or EAPTLS.</span></span> <span data-ttu-id="eb237-114">Quando EAPMSCHAPv2 é especificado, o cmdlet gera um instalador de configuração do cliente para autenticação de nome de usuário/senha que usa EAP-MSCHAPv2 protocolo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="eb237-114">When EAPMSCHAPv2 is specified then the cmdlet generates a client configuration installer for username/password authentication that uses EAP-MSCHAPv2 authentication protocol.</span></span> <span data-ttu-id="eb237-115">Se EAPTLS for especificado, o cmdlet gerará um instalador de configuração de cliente para autenticação de certificado que usa o protocolo EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="eb237-115">If EAPTLS is specified then the cmdlet generates a client configuration installer for certificate authentication that uses EAP-TLS protocol.</span></span> <span data-ttu-id="eb237-116">A opção "EapTls" pode ser usada para autenticação de certificado baseada em RAIO e autenticação de certificação executada pelo Gateway de Rede Virtual carregando a raiz confiável.</span><span class="sxs-lookup"><span data-stu-id="eb237-116">The "EapTls" option can be used for both RADIUS-based certificate authentication and certification authentication performed by the Virtual Network Gateway by uploading the trusted root.</span></span> <span data-ttu-id="eb237-117">O cmdlet detecta automaticamente o que está configurado.</span><span class="sxs-lookup"><span data-stu-id="eb237-117">The cmdlet automatically detects what is configured.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb237-118">-ClientRootCertificateFileList</span><span class="sxs-lookup"><span data-stu-id="eb237-118">-ClientRootCertificateFileList</span></span>
<span data-ttu-id="eb237-119">Uma lista de caminhos de certificado raiz do cliente</span><span class="sxs-lookup"><span data-stu-id="eb237-119">A list of client root certificate paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb237-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb237-120">-DefaultProfile</span></span>
<span data-ttu-id="eb237-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="eb237-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb237-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb237-122">-Name</span></span>
<span data-ttu-id="eb237-123">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="eb237-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb237-124">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="eb237-124">-ProcessorArchitecture</span></span>
<span data-ttu-id="eb237-125">Processorarchitecture</span><span class="sxs-lookup"><span data-stu-id="eb237-125">ProcessorArchitecture</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb237-126">-RadiusRootCertificateFile</span><span class="sxs-lookup"><span data-stu-id="eb237-126">-RadiusRootCertificateFile</span></span>
<span data-ttu-id="eb237-127">Caminho de certificado raiz do servidor de raios.</span><span class="sxs-lookup"><span data-stu-id="eb237-127">Radius server root certificate path.</span></span> <span data-ttu-id="eb237-128">Esse é um parâmetro obrigatório que deve ser especificado quando OEAP-TLS com autenticação RAIO é usado.</span><span class="sxs-lookup"><span data-stu-id="eb237-128">This is a mandatory parameter that has to be specified when EAP-TLS with RADIUS authentication is used.</span></span> <span data-ttu-id="eb237-129">Este é o nome completo do caminho do arquivo .cer que contém o certificado raiz RAIO que o cliente usa para validar o servidor RAIO durante a autenticação.</span><span class="sxs-lookup"><span data-stu-id="eb237-129">This is the full path name of .cer file containing the RADIUS root certificate that the client uses to validates the RADIUS server during authentication.</span></span>

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

### <span data-ttu-id="eb237-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb237-130">-ResourceGroupName</span></span>
<span data-ttu-id="eb237-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eb237-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb237-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="eb237-132">-Confirm</span></span>
<span data-ttu-id="eb237-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb237-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb237-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb237-134">-WhatIf</span></span>
<span data-ttu-id="eb237-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="eb237-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb237-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eb237-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb237-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb237-137">CommonParameters</span></span>
<span data-ttu-id="eb237-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb237-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb237-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb237-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb237-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="eb237-140">INPUTS</span></span>

### <span data-ttu-id="eb237-141">System.String</span><span class="sxs-lookup"><span data-stu-id="eb237-141">System.String</span></span>

### <span data-ttu-id="eb237-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="eb237-142">System.String[]</span></span>

## <span data-ttu-id="eb237-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="eb237-143">OUTPUTS</span></span>

### <span data-ttu-id="eb237-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="eb237-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="eb237-145">Notas</span><span class="sxs-lookup"><span data-stu-id="eb237-145">NOTES</span></span>

## <span data-ttu-id="eb237-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb237-146">RELATED LINKS</span></span>

[<span data-ttu-id="eb237-147">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb237-147">Get-AzVpnClientConfiguration</span></span>](./Get-AzVpnClientConfiguration.md)
