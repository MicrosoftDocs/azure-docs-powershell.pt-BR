---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: caad6363e49d3ac3fe4e591fba860251c0a1d3c0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775346"
---
# <span data-ttu-id="cd935-101">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd935-101">New-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="cd935-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd935-102">SYNOPSIS</span></span>
<span data-ttu-id="cd935-103">Esse comando permite que os usuários criem o pacote de perfil VPN com base em configurações de VPN pré-configuradas no gateway VPN, além de algumas configurações adicionais que os usuários podem precisar configurar, por exemplo, alguns certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="cd935-103">This command allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="cd935-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd935-104">SYNTAX</span></span>

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-ProcessorArchitecture <String>] -AuthenticationMethod <String> [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd935-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cd935-105">DESCRIPTION</span></span>
<span data-ttu-id="cd935-106">Isso permite que os usuários criem o pacote de perfil VPN com base em configurações de VPN pré-configuradas no gateway VPN, além de algumas configurações adicionais que os usuários podem precisar configurar, por exemplo, alguns certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="cd935-106">this allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="cd935-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cd935-107">EXAMPLES</span></span>

### <span data-ttu-id="cd935-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cd935-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

<span data-ttu-id="cd935-109">Esse cmdlet é usado para criar um arquivo zip do perfil do cliente VPN para "ContosoVirtualNetworkGateway" no grupo de Resource "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="cd935-109">This cmdlet is used to create a VPN client profile zip file for "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span></span> <span data-ttu-id="cd935-110">O perfil é gerado para um servidor RADIUS pré-configurado que é configurado para usar o método de autenticação "EAPTLS" com o arquivo de certificado VpnProfileRadiusCert.</span><span class="sxs-lookup"><span data-stu-id="cd935-110">The profile is generated for a pre-configured radius server that is configured to use "EAPTLS" authentication method with the VpnProfileRadiusCert certificate file.</span></span>

## <span data-ttu-id="cd935-111">OS</span><span class="sxs-lookup"><span data-stu-id="cd935-111">PARAMETERS</span></span>

### <span data-ttu-id="cd935-112">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="cd935-112">-AuthenticationMethod</span></span>
<span data-ttu-id="cd935-113">O método de autenticação pode ter os valores EAPMSCHAPv2 ou EAPTLS.</span><span class="sxs-lookup"><span data-stu-id="cd935-113">Authentication Method Can take values EAPMSCHAPv2 or EAPTLS.</span></span> <span data-ttu-id="cd935-114">Quando EAPMSCHAPv2 é especificado, o cmdlet gera um instalador de configuração de cliente para autenticação de nome de usuário/senha que usa o protocolo de autenticação EAP-MSCHAPv2.</span><span class="sxs-lookup"><span data-stu-id="cd935-114">When EAPMSCHAPv2 is specified then the cmdlet generates a client configuration installer for username/password authentication that uses EAP-MSCHAPv2 authentication protocol.</span></span> <span data-ttu-id="cd935-115">Se EAPTLS for especificado, o cmdlet gerará um instalador de configuração de cliente para autenticação de certificado que usa o protocolo EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="cd935-115">If EAPTLS is specified then the cmdlet generates a client configuration installer for certificate authentication that uses EAP-TLS protocol.</span></span> <span data-ttu-id="cd935-116">A opção "EapTls" pode ser usada para autenticação de certificação e autenticação de certificado baseada em RADIUS realizada pelo gateway de rede virtual carregando a raiz confiável.</span><span class="sxs-lookup"><span data-stu-id="cd935-116">The "EapTls" option can be used for both RADIUS-based certificate authentication and certification authentication performed by the Virtual Network Gateway by uploading the trusted root.</span></span> <span data-ttu-id="cd935-117">O cmdlet detecta automaticamente o que está configurado.</span><span class="sxs-lookup"><span data-stu-id="cd935-117">The cmdlet automatically detects what is configured.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: EAPTLS, EAPMSCHAPv2

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd935-118">-ClientRootCertificateFileList</span><span class="sxs-lookup"><span data-stu-id="cd935-118">-ClientRootCertificateFileList</span></span>
<span data-ttu-id="cd935-119">Uma lista de caminhos de certificado raiz do cliente</span><span class="sxs-lookup"><span data-stu-id="cd935-119">A list of client root certificate paths</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd935-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd935-120">-DefaultProfile</span></span>
<span data-ttu-id="cd935-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cd935-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="cd935-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd935-122">-Name</span></span>
<span data-ttu-id="cd935-123">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="cd935-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd935-124">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="cd935-124">-ProcessorArchitecture</span></span>
<span data-ttu-id="cd935-125">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="cd935-125">ProcessorArchitecture</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Amd64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd935-126">-RadiusRootCertificateFile</span><span class="sxs-lookup"><span data-stu-id="cd935-126">-RadiusRootCertificateFile</span></span>
<span data-ttu-id="cd935-127">Caminho do certificado raiz do servidor RADIUS.</span><span class="sxs-lookup"><span data-stu-id="cd935-127">Radius server root certificate path.</span></span> <span data-ttu-id="cd935-128">Esse é um parâmetro obrigatório que deve ser especificado quando EAP-TLS com autenticação RADIUS for usado.</span><span class="sxs-lookup"><span data-stu-id="cd935-128">This is a mandatory parameter that has to be specified when EAP-TLS with RADIUS authentication is used.</span></span> <span data-ttu-id="cd935-129">Esse é o nome do caminho completo do arquivo. cer que contém o certificado raiz RADIUS que o cliente usa para validar o servidor RADIUS durante a autenticação.</span><span class="sxs-lookup"><span data-stu-id="cd935-129">This is the full path name of .cer file containing the RADIUS root certificate that the client uses to validates the RADIUS server during authentication.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd935-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd935-130">-ResourceGroupName</span></span>
<span data-ttu-id="cd935-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cd935-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd935-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cd935-132">-Confirm</span></span>
<span data-ttu-id="cd935-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd935-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd935-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd935-134">-WhatIf</span></span>
<span data-ttu-id="cd935-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cd935-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd935-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cd935-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd935-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd935-137">CommonParameters</span></span>
<span data-ttu-id="cd935-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd935-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd935-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd935-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd935-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cd935-140">INPUTS</span></span>

### <span data-ttu-id="cd935-141">System. String</span><span class="sxs-lookup"><span data-stu-id="cd935-141">System.String</span></span>
<span data-ttu-id="cd935-142">System. Collections. Generic. List ' 1 [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="cd935-142">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="cd935-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cd935-143">OUTPUTS</span></span>

### <span data-ttu-id="cd935-144">Microsoft. Azure. Commands. Network. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="cd935-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="cd935-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cd935-145">NOTES</span></span>

## <span data-ttu-id="cd935-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd935-146">RELATED LINKS</span></span>
